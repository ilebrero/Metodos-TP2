CC = g++
CFLAGS = -std=c++11 -o

BINARIES = main matriz matrizsimetrica gauss descomposicionLU metodoPotencia PCA

.PHONY: main matriz matrizsimetrica gauss descomposicionLU PCA

all: $(BINARIES)

main: main.cpp
	$(CC) main.cpp clases/Matriz.cpp clases/MatrizSimetrica.cpp $(CFLAGS) main

mainTest: mainTest.cpp
	$(CC) mainTest.cpp clases/Matriz.cpp clases/MatrizSimetrica.cpp $(CFLAGS) mainTest

metodoPotencia:
	$(CC) metodos/metodoPotencia.cpp clases/Matriz.cpp clases/MatrizSimetrica.cpp $(CFLAGS) metodoPotencia

PLSDA:
	$(CC) metodos/PLSDA.cpp metodos/metodoPotencia.cpp clases/Matriz.cpp clases/MatrizSimetrica.cpp $(CFLAGS) PLSDA

PCA:
	$(CC) pca.cpp clases/Matriz.cpp clases/MatrizSimetrica.cpp $(CFLAGS) PCA

matriz: clases/Matriz.cpp
	$(CC) clases/Matriz.cpp $(CFLAGS) matriz

matrizsimetrica: clases/MatrizSimetrica.cpp
	$(CC) clases/MatrizSimetrica.cpp $(CFLAGS) matrizsimetrica

clean:
	rm -f ./*.o main
	rm -f ./*.o mainTest
	rm -f ./*.o metodoPotencia
	rm -f clases/*.o matriz
	rm -f clases/*.o matrizsimetrica
	rm -f clases/*.o PLSDA
