(

  # build fixes for jpeg 9 and glib2
  sedit "27 i typedef int boolean;\n#define HAVE_BOOLEAN" src/af/util/xp/ut_jpeg.cpp &&
  sedit "s:# *include <glib/[^>]*>:#include <glib.h>:" src/af/util/xp/ut_go_file.h goffice-bits/goffice/app/goffice-app.h &&

  sedit "s:--no-undefined:-no-undefined:" src/Makefile.in &&

  OPTS+=" --disable-static" &&

  default_build

) > $C_FIFO 2>&1
