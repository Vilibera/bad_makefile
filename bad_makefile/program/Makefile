#This is a Makefile

BIN:=main
SRC:=$(wildcard *.c)
OBJ:=$(SRC:.c=.o)

CFLAGS:=-Wall
CPPFLAGS:=-I$(shell pwd)

.PHONY: all clean

all: $(BIN)

$(BIN): $(OBJ)
	$(CC) $(CFLAGS) -o $@ $^

%.o: %.c
	$(CC) $(CFLAGS) $(CPPFLAGS) -c -o $@ $^

clean:
	$(RM) $(OBJ) $(BIN)
