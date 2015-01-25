AC_INIT([codeMonkey_scrm], [1.0-beta2],[https://github.com/paulstaab/scrm/issues])
AM_INIT_AUTOMAKE([subdir-objects -Wall -Werror foreign])

m4_ifndef([AM_SILENT_RULES], [m4_define([AM_SILENT_RULES],[])])
AM_SILENT_RULES([yes]) # Turn off all the compiling calls

AC_PROG_INSTALL
AC_PREREQ
AC_CANONICAL_HOST

# Checks for programs.
AC_PROG_RANLIB

# Checks for header files for scrm.
AC_HEADER_STDC
AC_LANG(C++) 

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_C_INLINE
AC_TYPE_SIZE_T

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
