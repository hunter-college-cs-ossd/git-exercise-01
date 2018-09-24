# A Makefile for compiling all of the programs in this directory
# Assumes each source file is a main program in either C or C++
# and that the C files have .c extension and C++ have .cpp extension.
# Executables should be copied into the ../bin directory and then 
# removed, so the sequence of a successful build is
# 	make
#	make install
# 	make clean

# Written by Stewart Weiss, September 23, 2018


CC         = /usr/bin/gcc
CXX        = /usr/bin/g++

C_SRCS    := $(wildcard *.c )
CXX_SRCS  := $(wildcard *.cpp )

C_EXECS   := $(patsubst %.c, %, $(C_SRCS))
CXX_EXECS := $(patsubst %.cpp, %, $(CXX_SRCS))

EXECS      = $(CXX_EXECS) $(C_EXECS)

CXXFLAGS  += -Wall -g 
CFLAGS    += -Wall -g 

.PHONY: all clean install

all:   $(EXECS)

clean:
	$(RM)  *.o $(EXECS)

install: $(EXECS)
	cp $(EXECS) ../bin

.cpp:
	$(CXX) $(CXXFLAGS) $@.cpp  -o $@

.c:
	$(CC) $(CFLAGS) $@.c  -o $@

