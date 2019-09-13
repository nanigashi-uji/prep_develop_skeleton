#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.61)
AC_INIT(prep_develop_skeleton, 0.0.1, [53845049+nanigashi-uji@users.noreply.github.com])
AM_INIT_AUTOMAKE

# Checks for programs.
#AC_PROG_CXX
#AC_PROG_CC
#AC_PROG_FC
#AC_PROG_F77
AC_PROG_INSTALL
#AC_PROG_RANLIB
#AC_PROG_LIBTOOL

# Checks for libraries.
#AC_CHECK_LIB(m,sqrt)

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_ARG_ENABLE(debug,
[  --enable-debug            trun on debugging [default no]])
if test "$enable_debug" = "yes"; then
   AC_DEFINE(DEBUG, 1, [Enable debug option of compiler])
else
   AC_DEFINE(DEBUG, 0, [Enable debug option of compiler])
  # CFLAGS="-DDEBUG $CFLAGS"
fi

# Checks for library functions.

datadir_exp=`eval echo ${datadir}`
datadirpath_exp=`eval echo ${datadir_exp}`

localstatedir_exp=`eval echo ${localstatedir}`
localstatedirpath_exp=`eval echo ${localstatedir_exp}`

bindir_exp=`eval echo ${prefix}/bin`
bindirpath_exp=`eval echo ${bindir_exp}`

PACKAGE_DATADIR_PATH=`eval echo ${datadirpath_exp}/${PACKAGE}`
PACKAGE_LOCALSTATEDIR_PATH=`eval echo ${localstatedirpath_exp}/run/${PACKAGE}`
PACKAGE_BINDIR_PATH=`eval echo ${bindirpath_exp}`

AC_SUBST(PACKAGE_DATADIR_PATH)
AC_SUBST(PACKAGE_LOCALSTATEDIR_PATH)
AC_SUBST(PACKAGE_BINDIR_PATH)

AC_DEFINE_UNQUOTED(PACKAGE_DATADIR_PATH,       "$PACKAGE_DATADIR_PATH", ["data dir"])
AC_DEFINE_UNQUOTED(PACKAGE_LOCALSTATEDIR_PATH, "$PACKAGE_LOCALSTATEDIR_PATH", ["local state dir"])
AC_DEFINE_UNQUOTED(PACKAGE_BINDIR_PATH,        "$PACKAGE_BINDIR_PATH", ["binary dir"])

module=no
eval DYLIB_EXT_M=\"$shrext_cmds\"
AC_SUBST(DYLIB_EXT_M)

AC_CONFIG_FILES([Makefile
                 bin/Makefile
                 bin/prep_develop_skeleton.sh
                 share/Makefile])
AC_OUTPUT

