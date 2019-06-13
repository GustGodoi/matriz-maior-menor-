# matriz-maior-menor-

package javaapplication1;

import java.util.Random;

public class JavaApplication1 {

    public static void main(String[] args) {
    
        Random aleatorio = new Random();

        String maior5 = "";
        String menor5 = "";
        String maiorPosicao7 = "";
        String menorPosicao7 = "";
        
        int[][] matriz = new int[10][10];
        
        
        for (int linha = 0; linha < matriz.length; linha++) {
            for (int coluna = 0; coluna < matriz[linha].length; coluna++) {
                matriz[linha][coluna] = aleatorio.nextInt(10);
                
            }
            
        }
        int maiorNumero1 = matriz[5][0];
        int menorNumero1 = matriz[5][0];
        int maiorNumero2 = matriz[0][7];
        int menorNumero2 = matriz[0][7];
        
        
        for (int linha = 0; linha < matriz.length; linha++) {
            for (int coluna = 0; coluna < matriz[linha].length; coluna++) {
                System.out.print("[" + linha + "]" + "[" + coluna + "]" + " | " + matriz[linha][coluna] + "\t");
                if (linha == 5 & matriz[linha][coluna] > maiorNumero1 | coluna == 0) {
                    maiorNumero1 = matriz[linha][coluna];
                    maior5 = "[5][" + coluna + "]";
                }
                if (linha == 5 & matriz[linha][coluna] < menorNumero1 | coluna == 0) {
                    menorNumero1 = matriz[linha][coluna];
                    menor5 = "[5][" + coluna + "]";
                }
                 if (coluna  == 7 & matriz[linha][coluna] > maiorNumero2 | linha == 0) {
                    maiorNumero2 = matriz[linha][coluna];
                    maiorPosicao7 = "[" + linha + "][7]";
                }
                if (coluna  == 7 & matriz[linha][coluna] < menorNumero2 | linha == 0) {
                    menorNumero2 = matriz[linha][coluna];
                    menorPosicao7 = "[" + linha + "][7]";
                }
            }
            
            System.out.println("");
        }
        System.out.println("");
        System.out.println(maior5 + "" + maiorNumero1);
        System.out.println(menor5 + "" + menorNumero1);
        System.out.println(maiorPosicao7 + "" + maiorNumero2);
        System.out.println(menorPosicao7 + "" + menorNumero2);
    }

}
