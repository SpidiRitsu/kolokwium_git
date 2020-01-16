VER = 0.1
CC = g++

OBJS = main.o employee.o address.o
EXEC = myProgram

$(EXEC): $(OBJS)
	$(CC) -o $@ $+

%.o: %.cpp
	$(CC) -c $<

main.o: employee.h address.h

employee.o: address.h

clean:
	rm -f $(EXEC) $(OBJS)

.PHONY: clean