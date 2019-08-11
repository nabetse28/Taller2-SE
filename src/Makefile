GCC = gcc
HEADERS = /home/nabetse28/Documentos/TEC/SistemasEmbebidos/Talleres/Taller2/Taller2-SE/src/
BIB = biblioteca
LIBBIB = libbiblioteca
LBIB = lbiblioteca
CAL = calculadora

static:
	$(GCC) -I $(HEADERS) -c $(BIB).c
	ar rv $(LIBBIB).a $(BIB).o
	$(GCC) -L$(HEADERS) -I$(HEADERS) -o $(CAL) $(CAL).c -lbiblioteca -lm

dinamic:
	$(GCC) -I $(HEADERS) -fPIC -c $(BIB).c
	ld -o $(LIBBIB).so $(BIB).o -shared
	$(GCC) -o $(CAL) $(CAL).c -I $(HEADERS) -L$(HEADERS) -$(LBIB) -lm 

clean:
	rm *.o *.so *.a calculadora