TARGET = scanner
OBJECT = lex.yy.o symboltable.o 
CC = cc -g
LEX = flex
LIBS = -lfl 

scanner:	lex.yy.o symboltable.o
	$(CC) -o scanner lex.yy.o symboltable.o

symboltable.o: symboltable.c 
	$(CC) -c symboltable.c 

lex.yy.o: lex.yy.c 
	$(CC) -c lex.yy.c 

lex.yy.c: lexer.lex
	$(LEX) $(LIB) lexer.lex

clean:
	rm -f $(TARGET) $(OBJECT) 

