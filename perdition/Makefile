######################################################################
# Makefile.popmap                                        February 2000
# Horms                                             horms@verge.net.au
#
# Make file to build a GDBM popmap.gdbm.db and a Berkeley DB 
# popmap.bdb.db from an ASCII popmap using makegdbm and makebdm
# respectivly.
#
# perdition
# Mail retrieval proxy server
# Copyright (C) 1999-2005  Horms
# 
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License as
# published by the Free Software Foundation; either version 2 of the
# License, or (at your option) any later version.
# 
# This program is distributed in the hope that it will be useful, but
# WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
# General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software Foundation,
# Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301, USA.
#
######################################################################

BINDIR=/usr/bin
MAKEBDB=$(BINDIR)/makebdb
MAKEGDBM=$(BINDIR)/makegdbm

.PHONY = all clean

all: popmap.gdbm.db popmap.bdb.db

popmap.gdbm.db: popmap
	test ! -x $(MAKEGDBM) || $(MAKEGDBM) $@ < popmap

popmap.bdb.db: popmap
	test ! -x $(MAKEBDB) || $(MAKEBDB) $@ < popmap

clean:
	rm -f popmap.gdbm.db popmap.bdb.db *~ *.bak core
