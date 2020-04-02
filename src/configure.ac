#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([FULL-PACKAGE-NAME], [VERSION], [BUG-REPORT-ADDRESS])

# Checks for programs.
AC_PATH_PROG([GFORTRAN_DIR],[gfortran])
AC_SUBST([GFORTRAN_DIR])

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lMetReader':
AC_CHECK_LIB([MetReader], [main])
# FIXME: Replace `main' with a function in `-lfftw3':
AC_CHECK_LIB([fftw3], [main])
# FIXME: Replace `main' with a function in `-lgrib_api':
AC_CHECK_LIB([grib_api], [main])
# FIXME: Replace `main' with a function in `-lgrib_api_f90':
AC_CHECK_LIB([grib_api_f90], [main])
# FIXME: Replace `main' with a function in `-lhourssince':
AC_CHECK_LIB([hourssince], [main])
# FIXME: Replace `main' with a function in `-llapack':
AC_CHECK_LIB([lapack], [main])
# FIXME: Replace `main' with a function in `-lm':
AC_CHECK_LIB([m], [main])
# FIXME: Replace `main' with a function in `-lnetcdf':
AC_CHECK_LIB([netcdf], [main])
# FIXME: Replace `main' with a function in `-lnetcdff':
AC_CHECK_LIB([netcdff], [main])
# FIXME: Replace `main' with a function in `-lnrlmsis':
AC_CHECK_LIB([nrlmsis], [main])
# FIXME: Replace `main' with a function in `-lprojection':
AC_CHECK_LIB([projection], [main])

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([makefile])
AC_OUTPUT
