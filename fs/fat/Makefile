#
#
# See file CREDITS for list of people who contributed to this
# project.
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License as
# published by the Free Software Foundation; either version 2 of
# the License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston,
# MA 02111-1307 USA
#

#TOPDIR=../../
#
#include $(TOPDIR)/config.mk

include ../../config.mk

LIB	= libfat.a
LIBS	= -L../tsk -ltsk

AOBJS	=
COBJS	= fat.o file.o

OBJS	= $(AOBJS) $(COBJS)

all:	$(LIB) $(AOBJS)

$(LIB):	.depend $(OBJS)
	$(AR) crv $@ $(OBJS)


#########################################################################

.depend:	Makefile $(AOBJS:.o=.S) $(COBJS:.o=.c)
		$(CC) -M $(CFLAGS) $(AOBJS:.o=.S) $(COBJS:.o=.c) > $@

sinclude .depend

#########################################################################