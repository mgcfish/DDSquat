DDSquat.pl
Kirk Greene <kgreene@directdefense.com>
http://www.DirectDefense.com

INTRODUCTION
============

Script that is an extension to URLCrazy (by  Andrew Horton -
http://www.morningstarsecurity.com/research/urlcrazy) that 
attempts to do some of the leg work/validation after getting
results of URLCrazy.

FEATURES
========

The following script was written to automate the validation
process of results generated by using URLCrazy. The script 
completes the following tasks:
 
  1) Runs a default URLCrazy session agains a provided domain
	2) Resulting domains that resolve are then:
		a) Submitted to a Whois check
		b) Arin lookups are done on the resolved IP address
		c) Screen captures are then taken of the site

CONSIDERATIONS
==============

1. You need to supply your own Snapito API key 	http://snapito.com/paid-api.jsp.
   Edit the script and place the key inbetween the quotes.

2. Unless URLCrazy is in your PATH, you will need to edit the script and 
   place the path to your urlcrazy (ex. "/pentest/urlcrazy-x.x/").
	
3. The following perl modules are used:
   IO::File

Finally, being a perl script, the script should run on almost any 
platform. The script was though written and tested on Ubuntu 12.x.

USAGE
=====

Running this script:

Usage:

	perl DDSquat.pl <domain>

	Exmaple:
	perl DDSquat.pl abc.com

 End result will be a report file (<domain_ddsquat_rpt.html>) and png 
 images placed within the <domain>_imgs folder of the directory you ran
 the script from. Images will be named after the domain they were taken
 for (ex. abc.com.png).

COPYRIGHT
=========

DDSquat.pl
Created by Kirk Greene
Copyright (C) 2013 DirectDefense, Inc.
 
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
 
You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>
