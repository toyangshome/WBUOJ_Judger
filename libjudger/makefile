test: test.o run.o
	@g++ -o test test.o run.o

test.o: test.cpp
	@gcc -c test.cpp

run.o: run.cpp
	@gcc -c run.cpp

.PHONY: clean
clean:
	@rm -f test test.o run.o