# Makefile for generating an LZMA library using Emscripten.

O = lzma
OBJECTS = \
  $(O)/Alloc.c \
  $(O)/LzFind.c \
  $(O)/LzmaDec.c \
  $(O)/LzmaEnc.c

all: lzma.a

%.o: %.c
	$(CC) -I. $< -o $@ -O2 -c

lzma.a: $(OBJECTS)
	$(AR) rvs $@ $(OBJECTS)

clean:
	rm lzma.a

