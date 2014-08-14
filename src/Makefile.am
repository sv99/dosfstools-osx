AM_CFLAGS = -O2 -fomit-frame-pointer -Wextra -Wno-sign-compare \
    -Wno-missing-field-initializers -Wmissing-prototypes -Wstrict-prototypes \
    -Wimplicit-function-declaration

AM_CPPFLAGS = -I../include
include_HEADERS = boot.h charconv.h check.h common.h fat.h file.h io.h lfn.h \
    version.h fsck.fat.h 

bin_PROGRAMS = fsck.fat mkfs.fat
mkfs_fat_SOURCES = mkfs.fat.c 
fsck_fat_SOURCES = fsck.fat.c boot.c check.c common.c fat.c file.c io.c lfn.c \
    charconv.c
