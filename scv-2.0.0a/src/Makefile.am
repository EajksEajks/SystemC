## ****************************************************************************
##
##  Licensed to Accellera Systems Initiative Inc. (Accellera) 
##  under one or more contributor license agreements.  See the 
##  NOTICE file distributed with this work for additional 
##  information regarding copyright ownership. Accellera licenses 
##  this file to you under the Apache License, Version 2.0 (the
##  "License"); you may not use this file except in compliance
##  with the License.  You may obtain a copy of the License at
## 
##    http://www.apache.org/licenses/LICENSE-2.0
## 
##  Unless required by applicable law or agreed to in writing,
##  software distributed under the License is distributed on an
##  "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
##  KIND, either express or implied.  See the License for the
##  specific language governing permissions and limitations
##  under the License.
##  
## ****************************************************************************
##
##  Makefile.am --
##  Process this file with automake to produce a Makefile.in file.
## 
## ****************************************************************************
##
##  Original Authors:
##  Norris Ip, Dean Shea, John Rose, Jasvinder Singh, William Paulsen,
##  John Pierce, Rachida Kebichi, Ted Elkind, David Bailey,
##  Cadence Design Systems, Inc., 2002-09-23
##
## ****************************************************************************
##  
##  MODIFICATION LOG - modifiers, enter your name, affiliation, date and
##  changes you are making here.
##
##      Name, Affiliation, Date:
##  Description of Modification:
##
## ****************************************************************************

## The order that these are processed in is important since
## scv depends on cudd and cudd needs scv_config.h ... etc.

SUBDIRS = \
	. cudd scv

include_HEADERS = scv.h

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = scv.pc

SCV_CONFIG= scv/scv_config.h

nodist_noinst_HEADERS = \
	$(SCV_CONFIG)

$(SCV_CONFIG): $(top_builddir)/config/config.h
	rm -f $@ $@.tmp
	cp $< $@.tmp
	echo "#undef PACKAGE" >>$@.tmp
	mv $@.tmp $@

CLEANFILES = \
	$(SCV_CONFIG)


