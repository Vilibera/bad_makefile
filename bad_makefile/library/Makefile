CC:=gcc
CFLAGS:=-Wall -fpic -shared
LIB:=Libcalculator.so
LIB_OBJ:=math_functions.c

PREFIX?=/usr

.PHONY: all install uninstall

all: $(LIB)

$(LIB):$(LIB_OBJ)
	$(CC) $(CFLAGS) -o $(LIB)  $^

install: $(LIB)
	install -d $(PREFIX)/include $(PREFIX)/lib
	install -m 644 $(LIB_OBJ) $(PREFIX)/include
	install -m 644 $(LIB) $(PREFIX)/lib

uninstall:
	$(RM) $(PREFIX)/include/$(LIB_OBJ)
	$(RM) $(PREFIX)/lib/$(LIB)
clean:
	$(RM) $(LIB)

