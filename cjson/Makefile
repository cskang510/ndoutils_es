OBJ = cJSON.o
LIBNAME = libcjson

R_CFLAGS = -fpic $(CFLAGS) -Wall -Werror -Wstrict-prototypes -Wwrite-strings -D_POSIX_C_SOURCE=200112L

## static lib
STLIBNAME = $(LIBNAME).a

.PHONY: all clean install

all: $(STLIBNAME)

$(STLIBNAME): $(OBJ)
		ar rcs $@ $<

$(OBJ): cJSON.c cJSON.h 

.c.o:
		$(CC) -ansi -pedantic -c $(R_CFLAGS) $<

clean: 
		rm -rf $(DYLIBNAME) $(STLIBNAME) *.o

distclean: clean
