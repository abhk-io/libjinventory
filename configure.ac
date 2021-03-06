#			-*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])

AC_CONFIG_MACRO_DIR([m4])

GENERIC_MAJOR_VERSION=2
GENERIC_MINOR_VERSION=0
GENERIC_MICRO_VERSION=0

GENERIC_VERSION=$GENERIC_MAJOR_VERSION.$GENERIC_MINOR_VERSION.$GENERIC_MICRO_VERSION
GENERIC_RELEASE=$GENERIC_MAJOR_VERSION.$GENERIC_MINOR_VERSION
AC_SUBST(GENERIC_RELEASE)
AC_SUBST(GENERIC_VERSION)

VERSION=$GENERIC_VERSION

#base
AC_INIT([libjinventory],[2.0],[jentenma@us.ibm.com])
AM_INIT_AUTOMAKE([-Wall subdir-objects -Werror foreign])
AC_CONFIG_HEADERS([config.h])


# check for libraries
#LIBS="-ludev -ljson-c"
AC_CHECK_LIB(udev,udev_new)
AC_CHECK_LIB(json-c,json_object_get)

#programs
AC_LANG([C++])
AC_PROG_CC
AC_PROG_CXX
AC_PROG_CPP
AC_C_CONST
AC_C_INLINE
AC_HEADER_STDBOOL
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AM_PROG_AR
AC_PROG_LIBTOOL
AC_SUBST(LIBTOOL_DEPS)


#headers
AC_HEADER_STDBOOL
AC_TYPE_SIZE_T
AC_HEADER_DIRENT
AC_HEADER_STDC
AC_CHECK_HEADERS([json-c/json.h libudev.h fcntl.h stdlib.h string.h sys/ioctl.h sys/param.h syslog.h unistd.h ctype.h])

#libraries
AC_FUNC_CLOSEDIR_VOID
AC_PROG_GCC_TRADITIONAL
AC_FUNC_LSTAT
AC_FUNC_LSTAT_FOLLOWS_SLASHED_SYMLINK
AC_HEADER_MAJOR
AC_FUNC_MALLOC
AC_FUNC_STAT
AC_CHECK_FUNCS([memmove memset mkdir socket strdup strerror strtol uname ])

#finished
AC_CONFIG_FILES([Makefile src/Makefile])
AC_OUTPUT
