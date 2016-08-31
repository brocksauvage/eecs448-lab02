#	Author: John Gibbons
#	Date: 2015.11.18


#make clean then make the exectuable by default
#standard "make clean" still works


.PHONY: prog main.o Test_LinkedList.o Test.o clean

prog: main.o Test.o Test_LinkedList.o
	clang++ -g -Wall -std=c++11 -stdlib=libc++ main.o Test.o Test_LinkedList.o -o prog


main.o: main.cpp LinkedList.h Node.h Test_LinkedList.h
	clang++ -g -Wall -std=c++11 -stdlib=libc++ -c main.cpp


Test_LinkedList.o: Test_LinkedList.h Test_LinkedList.cpp Test.h
	clang++ -g -Wall -std=c++11 -c Test_LinkedList.cpp

Test.o: Test.h Test.cpp
	clang++ -g -Wall -std=c++11 -stdlib=libc++ -c Test.cpp

#force returning true to prevent the default make from
#	haulting when .o files aren't present
clean:
	rm *.o *.*~ prog || true
