yaml --- layout: page title: Jekyll On CentOS 6 ---

1. yum -y install libxslt-devel libyaml-devel \
	libxml2-devel gdbm-devel libffi-devel \
	zlib-devel openssl-devel libyaml-devel \
	readline-devel curl-devel openssl-devel \
	pcre-devel git memcached-devel valgrind-devel \
	mysql-devel ImageMagick-devel ImageMagick

2. wget https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.0.tar.gz

3. wget https://rubygems.org/rubygems/rubygems-2.6.7.tgz

4. tar -xvzf ruby-2.3.0.tar.gz

5. tar -xvzf rubygems-2.6.7.tgz

6. cd ruby-2.3.0; ./configure; make; sudo make install

7. cd rubygems-2.6.7

8. sudo /usr/local/bin/ruby setup.rb

9. sudo /usr/local/bin/gem install bundler

10. sudo /usr/local/bin/gem install jekyll

Ruby is not designed for a NIST 800-53 System that restricts SuperUser umask (0077).
SO.... SuperUser installations that prevent user modifications will break Ruby's 
internal management functions.  Naturally these trigger when even running as
a normal user, so the Ruby system permissions will need modification:

  find /usr/local/lib/ruby -type d -exec chmod go+rx {} \; 
  find /usr/local/lib/ruby -type f -exec chmod go+r {} \; 

Further, "Bundler" will automatically install and update GEMs whenever it is run, 
and these again inherit inaccessible permissions.  SO... "/usr/local/bin/gem install bundler" 
will fail and "/usr/local/bin/gem install jekyll" will fail.

To resolve this you will need to run:

!/bin/bash
while (true)
do
  find /usr/local/lib/ruby -type d -exec chmod go+rx {} \; 
  find /usr/local/lib/ruby -type f -exec chmod go+r {} \; 
  echo cycling....
done

With script in place you can now run "/usr/local/bin/gem install bundler" and allow the permissions to script to cycle.

FURTHER Still!!!  RubyGems and Bundler will fail whenever a GEM attempts to Compile and Install BINARIES!  
At this point you must manually install the GEM as root and allow the permissions script to cycle:

     1. gem install i18n -v '0.7.0'
     2. gem install nokogiri -v '1.6.7.2'
     3. gem install RedCloth -v '4.2.9'
     4. gem install ffi -v '1.9.10'
     5. gem install rdiscount -v '2.1.8'
     6. gem install nokogiri -v '1.6.7.2' -- --use-system-libraries

Finally "bundle exec jekyll build" will update stale GEMs and install the GitHub Pages GEM.
This again will inherit inaccessible permissions, so keep the script in place and keep running 
"bundle install" until all possible GEMs and Updates are exhausted.

The Documentation will finally build without any problems:

[openwis-documentation]$ bundle exec jekyll build
Configuration file: /home/marcg/OpenWIS-3.14/openwis-documentation/_config.yml
            Source: /home/marcg/OpenWIS-3.14/openwis-documentation
       Destination: /home/marcg/OpenWIS-3.14/openwis-documentation/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 3.312 seconds.
 Auto-regeneration: disabled. Use --watch to enable.

