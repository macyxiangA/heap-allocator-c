# heap-allocator-c

A custom dynamic memory allocator written in C.  
This project implements a heap allocator with best-fit placement, block splitting, and immediate coalescing, and provides an automated test workflow using Makefiles.

The allocator exposes a minimal public interface and is designed to be built as a shared library and validated through an extensive test suite.

## Project Structure

p3Heap.c  
    Core allocator implementation (heap initialization, allocation, free, coalescing)

p3Heap.h  
    Public interface for the allocator

Makefile  
    Builds the allocator as a shared object

tests/  
    Test programs and test Makefile for validating allocator behavior

.gitignore  
    Ignores build artifacts and editor files

README.md  
    Project documentation

## Allocator Features

- Best-fit allocation strategy
- Block size alignment to 8 bytes
- Block splitting when excess space is available
- Immediate coalescing with adjacent free blocks
- Footer-based free block tracking
- Shared library build for external testing

## Build Instructions

From the project root directory, build the allocator shared library:

    make p3Heap

This produces:

    p3Heap.o
    libheap.so

## Running Tests

Change into the tests directory:

    cd tests

Build all test executables:

    make

Run allocation-only tests:

    make partA

Run allocation and free tests (no coalescing):

    make partB

Run tests requiring immediate coalescing:

    make partC

Run advanced coalescing tests:

    make partD

## Memory Checking

To check for memory errors using valgrind:

    make memcheck

You may also run valgrind on individual test binaries.

## Cleaning Build Artifacts

Remove all generated binaries and object files:

    make clean

## Notes

- This repository contains only implementation code and test drivers.
- Generated binaries and shared objects are excluded via .gitignore.
- The allocator is designed to be tested through the provided test harness and Makefiles.
- The README is written to be portable and stable across GitHub, VS Code, and Markdown editors.

