# Name of the project
PROJ_NAME = UnitConverter


BUILD = build

# All source code files
SRC =prog1.c\
UnitConverterOperations.c

#project output
PROJECT_OUTPUT= $(BUILD)/$(PROJ_NAME)
#def
$(PROJ_NAME):all
#run
.PHONY: run clean test doc all
all: $(SRC) $(BUILD)
	gcc $(SRC) $(INC) -o $(PROJECT_OUTPUT).out

#call
run:$(PROJ_NAME)
	./$(PROJECT_OUTPUT).out

# Build and run the unit tests
test:$(BUILD)
	gcc $(TEST_SRC) $(INC) -o $(TEST_OUTPUT)
	./$(TEST_OUTPUT)
#Coverage
coverageCheck:$(BUILD)
	g++ -fprofile-arcs -ftest-coverage -fPIC -O0 $(TEST_SRC) $(INC) -o $(TEST_OUTPUT)
	./$(TEST_OUTPUT)
 
# Remove all the built files, invoke by `make clean`
clean:
	rm -rf $(BUILD) $(DOCUMENTATION_OUTPUT)
 
# Create new build folder if not present
$(BUILD):
	mkdir build
