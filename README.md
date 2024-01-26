# Trabajemos los arrays bidimensionales o matrices
## Pseudocódigo

      Programa Matrices
          // Definición de la matriz
          Entero matriz[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}}
      
          // Recorrido con while, la forma más incómoda
          Entero i = 0
          Mientras i < Longitud(matriz) Hacer
              Entero j = 0
              Mientras j < Longitud(matriz[i]) Hacer
                  Escribe matriz[i][j]
                  j = j + 1
              Fin Mientras
              i = i + 1
          Fin Mientras
    
      
          // Recorrido con for, la forma más cómoda
          Para i = 0 Hasta Longitud(matriz) Hacer
              Para j = 0 Hasta Longitud(matriz[i]) Hacer
                  Escribe matriz[i][j]
              Fin Para
          Fin Para
      
          // Escribir las columnas a la inversa
          Para i = 0 Hasta Longitud(matriz) Hacer
              Para j = Longitud(matriz[i]) - 1 Descendiendo Hasta 0 Hacer
                  Escribe matriz[i][j]
              Fin Para
          Fin Para
      
          // Escribir las filas a la inversa
          Para i = Longitud(matriz) - 1 Descendiendo Hasta 0 Hacer
              Para j = 0 Hasta Longitud(matriz[i]) Hacer
                  Escribe matriz[i][j]
              Fin Para
          Fin Para
      
          // Todo a la inversa, invertir la matriz
          Para i = Longitud(matriz) - 1 Descendiendo Hasta 0 Hacer
              Para j = Longitud(matriz[i]) - 1 Descendiendo Hasta 0 Hacer
                  Escribe matriz[i][j]
              Fin Para
          Fin Para
    
      Fin Programa

## Código Java

    public class Matrices {

    public static void main(String[] args) {
        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Recorremos con un while, la forma más incomoda
        int i = 0; // filas
        while (i < matrix.length) {
            int j = 0; // columnas
            while (j < matrix[i].length) {
                System.out.print(matrix[i][j] + " ");
                j++;
            }
            System.out.println();
            i++;
        }

        System.out.println();

        // con un for, la forma más cómoda
        for (i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix[i].length; j++) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println();

        // for each
        for (int[] fila : matrix) {
            for (int elemento : fila) {
                System.out.print(elemento + " ");
            }
            System.out.println();
        }

        System.out.println();

        // escribIMOS las columnas a la inversa
        for (i = 0; i < matrix.length; i++) {
            for (int j = matrix[i].length - 1; j >= 0; j--) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println();

        // escribo las filas a la inversa
        for (i = matrix.length - 1; i >= 0; i--) {
            for (int j = 0; j < matrix[i].length; j++) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println();

        // Todo a la inversa, es decir matriz inversa
        for (i = matrix.length - 1; i >= 0; i--) {
            for (int j = matrix[i].length - 1; j >= 0; j--) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println();
    }
}
