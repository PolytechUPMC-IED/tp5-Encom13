CC=gcc
CFLAGS=-O3 -Wall -funroll-loops
LDLIBS=-lpng
PROGRAMS=pbm2png pbm2eps9 
SOURCES_LIB= pbm2png.c pbm2eps9.c printer.c
OBJ=pbm2eps9.o printer.o

all: $(PROGRAMS)

pbm2png: pbm2png.c
	$(CC) $(CFLAGS) -s -o $@ pbm2png.c $(LDLIBS)

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $<

pbm2eps9: $(OBJ)
	$(CC) -s -o $@ $(OBJ)

clean:
	rm -f $(PROGRAMS) $(OBJ)

.depend:
	gcc -MM ${SOURCE_LIB} > $@

-include .depend

.PHONY: all clean
