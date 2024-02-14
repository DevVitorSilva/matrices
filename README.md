# Matrices 

Criar um programa para ler um número inteiro N e 
uma matriz de ordem N contendo números inteiros. Em 
seguida, mostrar a diagonal principal e a quantidade 
de valores negativos da matriz.

```java
import java.util.Locale;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Locale.setDefault(Locale.US);
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a length for the array: ");
        int length = sc.nextInt();
        int[][] array = new int[length][length];
        int[] mainDiagonal = new int[length];
        int negativeNumber = 0;
        for(int i = 0; i < length; i++){
            for(int i2 = 0; i2 < length; i2++){
                array[i][i2] = sc.nextInt();
                if(array[i][i2] < 0){
                    negativeNumber++;
                }
            }
            mainDiagonal[i] = array[i][i];
        }
        System.out.println("Main diagonal:");
        for(int diagonal : mainDiagonal){
            System.out.print(diagonal + " ");
        }
        System.out.println("\nNegative numbers: " + negativeNumber);
        sc.close();
    }
}
```