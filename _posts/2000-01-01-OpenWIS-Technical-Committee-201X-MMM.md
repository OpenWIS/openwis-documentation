---
layout: page
title: A Markdown template for OpenWIS meeting minutes
---

Note: You should change the 'title' in the yaml above to the title of the meeting, eg:
OpenWIS Technical Committee 2016 May

#### DDth (FULL MONTH NAME) 2016 - teleconference - meeting minutes

---
(horizontal rule)

1. **lh level 1 (strong em)**
	1. **lh level 2 (strong em)**
		1. lh level 3 or lower (no-em)
			1. li 1
			2. _li 2 (weak em)_
			3. ACT-OWIS-TC-99:Action: XX - Note the opening and closing tags that markup this as an ACTION. OWIS-ACT
2. **lh level 1**
	1. li 1
	2. RES-OWIS-TC-99:Resolution: Note the opening and closing tags that markup this as a RESOLUTION. OWIS-RES
	3. **lh level 2 (strong em)**
		1. > blockquote
		2. li 2
3. **unordered list**
	- ul li 1
	- ul li 2
4. Links: (to see what is going on here, open the file as plain text, or refer to the Markdown docs)
	- [inline ref to external link](http://www.example.com)
	- [ref to link defined somewhere else on this page][L1]
	- [link to local static assets that are stored in the /assets/ folder that is in the folder structure of the site ][assets]

[L1]: http://www.example.com
[assets]: {{ site.baseurl | prepend: site.url }}/assets/filename


---
(horizontal rule)

#### Participants

- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM]
- YW - Yang Wang, Bureau of Meteorology, Australia [BoM]
- BB - Bruce Bannerman, Bureau of Meteorology, Australia [BoM]

- OL - Okki Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- HL - Hyekyoung Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- SP - Sungeun Park, Korea Meteorological Administration, Republic of Korea [KMA]
- CSP - Chung Shin Park, Korea Meteorological Administration, Republic of Korea [KMA]

- MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
- MV - Mikko Visa, Finnish Meteorological Institute, Finland [FMI]

- MDA - Matteo Dell'Acqua, Meteo France, France [MF], Chair
- RGr - Remy Giraud, Meteo France, France [MF]
- MC - Michael Claudon, Meteo France, France [MF]
- YG - Yves Goupil, Meteo France, France [MF]
- JP - Jean Perie, Meteo France, France [MF]

- RGb - Remy Gibault, Meteo France International, France [MFI]
- LLG - Loic Le Gallou, Meteo France International, France [MFI], Vice-Chair

- SO - Steve Olson, National Weather Service, USA [NWS], Vice-Chair
- PG - Patrick Gillis, National Weather Service, USA [NWS]
- KS - Kari Sheets, National Weather Service, USA [NWS]
- MGi - Marc Giannoni, National Weather Service, USA [NWS]

- BR - Baudouin Raoult, European Centre for Medium Range Weather Forecasting [ECMWF]

- JT - Jeremy Tandy, Met Office, UK [UKMO], Chair/Vice-Chair
- EE - Emma Edwards, Met Office, UK [UKMO], Treasurer
- MGo - Martin Gollogly, SCISYS, UK [UKMO]
- DJ - Duncan Jeffrey, Met Office, UK [UKMO]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- MR - Michael Robbins, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- JO - Julie Oakley, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]

- NM - Nassos Michas, European Dynamics, Greece [UKMO]
- GT - Giorgos Tryantafyllidis, European Dynamics, Greece [UKMO]
- DG - Dimitris Gianneler, European Dynamics, Greece [UKMO]
- DP - Dimitris Papadeas, European Dynamics, Greece [UKMO]

#### Apologies
- Robert Bunge, National Weather Service, USA [NWS]
