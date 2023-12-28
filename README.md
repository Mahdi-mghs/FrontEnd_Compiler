# FrontEnd_Compiler
FrontEnd Compiler project 

## Lexical Analysis
Describe _Library_ & ambgious function used in [lexil.l]()

**yylineno** : A lexical analyzer generator, When this option is included in the Lex file, it instructs Lex to keep track of the number of lines it has read from the input. Each time Lex reads a newline character, it increments `yylineno`.
> printf("Error on line %d: invalid character.\n", yylineno);

**yywrap** : It's a Wrapp function ( Carry remaining words to another line ), when it's done return 1 else 0

**yylex** : Call invoke lexer, final tokenizing for parser

## Parser & Symbol Table

In some of section code we have repeated grammer in one rule like
> headers: headers headers
> | INCLUDE
> ;

`Bing AI`: This means that a headers can consist of two headers in sequence. This is a recursive rule, which allows for any number of headers to appear in sequence.

In other word we could say our header follow another header

### Next Part
We have a `Struct datatype` for Symbol table, contains ID, Data_Type, Type, Line_number and also for mini code size was setelled 40 elements

### Conclusion
You can check final result with _a.out_ file
> ./a.out<test.c command in linux
***
Provided by [Mahdi-Mghs](https://github.com/Mahdi-mghs/)
