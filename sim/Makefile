#!/bin/bash

.PHONY  : clean

CC      = gcc
CXX     = g++
CFLAGS  = -o  
VCOM    = iverilog
VFLAGS  = -o
VRUN    = vvp

VSRC    = hello.v
TARGET  = hello

CSRC    = $(wildcard *.c)
COBJ    = $(patsubst %.c, %.o, $(wildcard *.c))

(TARGET) : $(COBJ)
	$(CXX) $(CFAGS) $@ $<

%.o       : %.c
	$(CXX) $(CFAGS) $@ $<

vrun      : $(TARGET)
	$(VRUN) $<

%         : %.v
	$(VCOM) $(VFLAGS) $@ $<

clean     :
	rm -rf $(TARGET)
