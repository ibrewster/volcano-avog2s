#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([FULL-PACKAGE-NAME], [VERSION], [BUG-REPORT-ADDRESS])

AC_PATH_PROG([GFORTRAN_DIR],[gfortran])
AC_SUBST([GFORTRAN_DIR])

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lMetReader':
AC_CHECK_LIB([MetReader], [main])
# FIXME: Replace `main' with a function in `-lfftw3':
AC_CHECK_LIB([fftw3], [main])

FOUND_GRIB=0
FOUND_GRIB_F90=0
# FIXME: Replace `main' with a function in `-lgrib_api':
AC_CHECK_LIB([grib_api], [main],[FOUND_GRIB=1])
# FIXME: Replace `main' with a function in `-lgrib_api_f90':
AC_CHECK_LIB([grib_api_f90], [main],[FOUND_GRIB_F90=1])

FOUND_ECCODES=0
FOUND_ECCODES_F90=0
# FIXME: Replace `main' with a function in `-leccodes':
AC_CHECK_LIB([eccodes], [main],[FOUND_ECCODES=1])
# FIXME: Replace `main' with a function in `-leccodes_f90':
AC_CHECK_LIB([eccodes_f90], [main],[FOUND_ECCODES_F90=1])

if test $FOUND_ECCODES -eq 1 -a $FOUND_ECCODES_F90 -eq 1; then
    ECCODES_AVAIL=1
else
    ECCODES_AVAIL=0
fi

if test $FOUND_GRIB -eq 1 -a $FOUND_GRIB_F90 -eq 1; then
    GRIB_AVAIL=1
else
    GRIB_AVAIL=0
fi

if test $GRIB_AVAIL -eq 1; then
    DATALIBS="-lnetcdf -lnetcdff -lgrib_api_f90 -lgrib_api"
else 
    if test $ECCODES_AVAIL -eq 1; then
        DATALIBS="-lnetcdf -lnetcdff -leccodes -leccodes_f90"
    else
        AC_MSG_ERROR([At least one of grib_api or eccodes is required, neither found.])
    fi
fi

AC_SUBST([DATALIBS])

# FIXME: Replace `main' with a function in `-lhourssince':
AC_CHECK_LIB([hourssince], [main],[],[AC_MSG_ERROR([Required library "hourssince" not found])])
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
AC_CHECK_LIB([HWM14],[main])

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([makefile ExternalDataSoftware/makefile_HWM14])
AC_OUTPUT
