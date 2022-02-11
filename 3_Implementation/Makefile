#Target_name : Dependencies
#<TAB>Commmand
SRC = snakegame.c\
src/snake.c
INC = inc
all.out : $(SRC)
    gcc $^ -I$(INC) -o $@
run: target
    ./all.out
clean:
    rm all.out
# Document the code using Doxygen
doc:
	make -C ./documentation

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