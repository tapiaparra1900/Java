import java.util.Scanner;

public class pract1  {
    public static void main(String[] args) {
        Scanner leer = new Scanner(System.in);
        int repetir = 1;

        while (repetir == 1) {
            double num1, num2, num3;
            double mayor, medio, menor, promedio;

            System.out.println("Ingresa el primer numero:");
            num1 = leer.nextDouble();

            System.out.println("Ingresa el segundo numero:");
            num2 = leer.nextDouble();

            System.out.println("Ingresa el tercer numero:");
            num3 = leer.nextDouble();

            promedio = (num1 + num2 + num3) / 3;

           
            if (num1 >= num2 && num1 >= num3) {
                mayor = num1;
                if (num2 >= num3) {
                    medio = num2;
                    menor = num3;
                } else {
                    medio = num3;
                    menor = num2;
                }
            } else if (num2 >= num1 && num2 >= num3) {
                mayor = num2;
                if (num1 >= num3) {
                    medio = num1;
                    menor = num3;
                } else {
                    medio = num3;
                    menor = num1;
                }
            } else {
                mayor = num3;
                if (num1 >= num2) {
                    medio = num1;
                    menor = num2;
                } else {
                    medio = num2;
                    menor = num1;
                }
            }

            System.out.println("\n Resultados ");
            System.out.println("Numero mayor: " + mayor);
            System.out.println("Numero medio: " + medio);
            System.out.println("Numero menor: " + menor);
            System.out.println("Promedio: " + promedio);

            System.out.println("\nDeseas realizar otra operacion?");
            System.out.println("1. Si");
            System.out.println("Cualquier otro numero. No");
            repetir = leer.nextInt();

            System.out.println();
        }

        System.out.println("Programa terminado");
        leer.close();
    }
}
