user-sh : bison.tab.o execute.o
	cc -o user-sh bison.tab.o lex.yy.o execute.o -lfl
bison.tab.o : bison global.h
	cc -c bison.tab.c lex.yy.c -ggdb
execute.o : execute.c global.h
	cc -c execute.c -ggdb
bison :	lex_analysis.l bison.y
	bison -d bison.y
	flex lex_analysis.l
	
clean :
	rm user-sh bison.tab.o bison.tab.h execute.o bison.tab.c lex.yy.o lex.yy.c *.tmp
