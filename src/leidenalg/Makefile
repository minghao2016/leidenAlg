CXX ?= g++
PKG_CXXFLAGS = -O3 -std=c++11 -pthread -fPIC $(SHLIB_OPENMP_CXXFLAGS)
PKG_CXXFLAGS += -I"./include" -I"./igraph-R"
LDFLAGS += -lpthread


LIB = ../libleidenalg.a
lib: $(LIB)

$(LIB): CPMVertexPartition.o LinearResolutionParameterVertexPartition.o RBConfigurationVertexPartition.o SurpriseVertexPartition.o ModularityVertexPartition.o RBERVertexPartition.o GraphHelper.o MutableVertexPartition.o ResolutionParameterVertexPartition.o Optimiser.o SignificanceVertexPartition.o
	ar rvs $@ $?

clean:
	@-rm -f *.o $(LIB) 


