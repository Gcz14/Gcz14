package listaexercicios1;

import java.util.Scanner;

public class Exercicio18 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Insira de modo decrescente os valores a seguir: ");
        System.out.print("Insira o valor do lado A: ");
        double ladoA = sc.nextDouble();
        System.out.print("Insira o valor do lado B: ");
        double ladoB = sc.nextDouble();
        System.out.print("Insira o valor do lado C: ");
        double ladoC = sc.nextDouble();

        if (ladoA < ladoB || ladoB < ladoC) {
            System.out.println("Impossivel realizar os calculos! Os numeros precisam estar em ordem decrescente.");
        } else {

            double ladoA2 = ladoA * ladoA;
            double ladoB2 = ladoB * ladoB;
            double ladoC2 = ladoC * ladoC;

            if (ladoA >= ladoB + ladoC) {
                System.out.println("Nao forma triangulo.");
            } else if (ladoA2 == ladoB2 + ladoC2) {
                System.out.println("Triangulo retangulo.");
            } else if (ladoA2 > ladoB2 + ladoC2) {
                System.out.println("Triangulo obtusangulo.");
            } else {
                System.out.println("Triangulo acutÃ¢ngulo.");
            }

            if (ladoA == ladoB && ladoA == ladoC) {
                System.out.println("Triangulo equilatero.");
            } else if (ladoA == ladoB || ladoB == ladoC || ladoC == ladoA) {
                System.out.println("Triangulo isosceles.");
            }
        }
    }
}
