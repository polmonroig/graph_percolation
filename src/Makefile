# variable definition
OPT = -O3
STD = -std=c++17
COMPILER = g++ $(OPT)
PROGRAM_NAME = program
OUTNAME = -o $(PROGRAM_NAME)

# directory definition

RANDOM = random/rand_generator.cpp
GRAPH =  graph/graph.cpp graph/grid.cpp graph/geometric.cpp graph/triangular_grid.cpp
DATA =   data/csv_file.cpp
TREE = tree/hyperrectangle.cpp tree/kd_tree.cpp tree/node.cpp
MAIN = $(PROGRAM_NAME).cpp


TARGET = $(RANDOM) $(GRAPH) $(DATA) $(TREE)

# rule definition
program: $(TARGET) $(MAIN) $(TARGET:.cpp=.h)
	$(COMPILER) $(STD) $(TARGET) $(MAIN) $(OUTNAME) -pthread

clean:
		rm $(PROGRAM_NAME)
