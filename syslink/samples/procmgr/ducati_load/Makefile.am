#
#  Copyright 2001-2009 Texas Instruments - http://www.ti.com/
#
#  Licensed under the Apache License, Version 2.0 (the "License");
#  you may not use this file except in compliance with the License.
#  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.

PROJROOT=../..
INCLUDE = \
	-I $(PROJROOT)/../api/include \
	-I $(PROJROOT)/inc


AM_CFLAGS = -Wall -g -O2 $(INCLUDE) -finline-functions -D$(PROCFAMILY)

LDPATH=$(PROJROOT)/../api/src

API_LIBS = \
	$(LDPATH)/utils/libutils.la \
	$(LDPATH)/ipc/libipc.la \
	$(LDPATH)/procmgr/libprocmgr.la \
	$(LDPATH)/procmgr/procmgr4430/libomap4430proc.la\
	$(LDPATH)/sysmgr/libsysmgr.la \
	$(LDPATH)/notify/libnotify.la \
	$(LDPATH)/sysmemmgr/libsysmemmgr.la

bin_PROGRAMS = ducati_load.out

ducati_load_out_SOURCES = ducati_load.c getopt.c

ducati_load_out_CPPFLAGS = $(AM_CLFAGS)

ducati_load_out_LDADD = $(API_LIBS)

