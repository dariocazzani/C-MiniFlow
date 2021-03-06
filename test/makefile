CXX = g++ -std=c++11
DEBUG = -g
CFLAGS = -Wall -Wextra -Werror -pedantic $(DEBUG)

BUILDDIR := ../build/
TARGET := ../bin/

all: build
	@echo " Running tests..."
	$(TARGET)node_test
	$(TARGET)graph_test
	$(TARGET)sigmoid_test
	$(TARGET)MSE_test
	$(TARGET)linear_test
	$(TARGET)input_test
	$(TARGET)softmaxXent_test

first:
	@echo " Building tests..."

build: node_test graph_test sigmoid_test MSE_test linear_test input_test softmaxXent_test

node_test : node_test.o
	$(CXX) -o $(TARGET)node_test $(BUILDDIR)node_test.o

node_test.o: first node_test.cc
	$(CXX) $(CFLAGS) -c node_test.cc -o $(BUILDDIR)node_test.o

graph_test : graph_test.o
	$(CXX) -o $(TARGET)graph_test $(BUILDDIR)graph_test.o

graph_test.o: graph_test.cc
	$(CXX) $(CFLAGS) -c graph_test.cc -o $(BUILDDIR)graph_test.o

sigmoid_test : sigmoid_test.o
	$(CXX) -o $(TARGET)sigmoid_test $(BUILDDIR)sigmoid_test.o

sigmoid_test.o: sigmoid_test.cc
	$(CXX) $(CFLAGS) -c sigmoid_test.cc -o $(BUILDDIR)sigmoid_test.o

MSE_test : MSE_test.o
	$(CXX) -o $(TARGET)MSE_test $(BUILDDIR)MSE_test.o

MSE_test.o: MSE_test.cc
	$(CXX) $(CFLAGS) -c MSE_test.cc -o $(BUILDDIR)MSE_test.o

input_test : input_test.o
	$(CXX) -o $(TARGET)input_test $(BUILDDIR)input_test.o

input_test.o: input_test.cc
	$(CXX) $(CFLAGS) -c input_test.cc -o $(BUILDDIR)input_test.o

linear_test : linear_test.o
	$(CXX) -o $(TARGET)linear_test $(BUILDDIR)linear_test.o

linear_test.o: linear_test.cc
	$(CXX) $(CFLAGS) -c linear_test.cc -o $(BUILDDIR)linear_test.o

softmaxXent_test : softmaxXent_test.o
	$(CXX) -o $(TARGET)softmaxXent_test $(BUILDDIR)softmaxXent_test.o

softmaxXent_test.o: softmaxXent_test.cc
	$(CXX) $(CFLAGS) -c softmaxXent_test.cc -o $(BUILDDIR)softmaxXent_test.o
clean:
	rm -rf $(BUILDDIR)*.o $(TARGET)*

.PHONY: all run
