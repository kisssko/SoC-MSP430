# Copyright (c) 2015 by the author(s)
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
# THE SOFTWARE.
#
# Author(s):
#   Stefan Wallentowitz <stefan.wallentowitz@tum.de>

AC_PREREQ(2.60)
AC_INIT([gzll-libraries],
        [0.1],
        [stefan.wallentowitz@tum.de])

AC_CONFIG_AUX_DIR([build-aux])
AM_INIT_AUTOMAKE([check-news foreign 1.11 -Wall -Wno-portability silent-rules tar-pax no-dist-gzip dist-xz subdir-objects])

AM_PROG_AS
AC_PROG_CC_C99

AC_SYS_LARGEFILE
AC_CONFIG_MACRO_DIR([m4])
AM_SILENT_RULES([yes])

LT_INIT()

PKG_CHECK_MODULES([GZLL], [gzll-kernel])
AC_SUBST([GZLL_CFLAGS])


AM_CONDITIONAL([MSP430OBJDUMPSET],[test "x$MSP430OBJDUMP" != "x"])
AM_CONDITIONAL([MSP430OBJCOPYSET],[test "x$MSP430OBJCOPY" != "x"])
AC_SUBST(MSP430OBJDUMP)
AC_SUBST(MSP430OBJCOPY)

AC_CONFIG_FILES([
        Makefile
        src/Makefile
        src/libgzll/Makefile
])

AC_OUTPUT
