# Java
import java.util.Scanner;

public class subRotinas {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("=========================");
        System.out.println("      Calcular Área");
        System.out.println("=========================");

        System.out.println("Escolha qual gostária de calcular a Área: ");//Decisão do usuário em qual forma ele quer aplicar
        System.out.println("1) Retângulo");
        System.out.println("2) Triângulo");
        System.out.println("3) Trapézio");
        System.out.println("4) Círculo");

        System.out.print("R: ");
        int escolha = sc.nextInt(); // Coleta de Dados

        Forma(escolha); // Chamando o procedimento

    }
    public static void Forma(int a){ //Procedimento que define o que acontece pós escolha do usuário

        Scanner sc = new Scanner(System.in);

        if(a == 1){ // Adicionando condições que vaream de resposta
            System.out.println("=================--================");
            System.out.println("              Retângulo");
            System.out.println("=================--================");

            System.out.print("Informe a Base do retângulo: ");
            double base = sc.nextDouble();
            System.out.print("Informe a Altura do retângulo: ");
            double altura = sc.nextDouble();

            double area = base*altura;

            System.out.print("A área do seu retângulo: " + area + "m?");

        }
        else if(a == 2){
            System.out.println("=================--================");
            System.out.println("              Triângulo");
            System.out.println("=================--================");

            System.out.print("Informe a Base do Triângulo: ");
            double base = sc.nextInt();
            System.out.print("Informe a Altura do Triângulo: ");
            double altura = sc.nextDouble();

            double area = (base*altura)/2;
            System.out.print("A área do seu Triângulo: "+area+"m²");
        }
        else if(a == 3){
            System.out.println("=================--================");
            System.out.println("              Trapézio");
            System.out.println("=================--================");

            System.out.print("Informe a Base maior do Trapézio: ");
            double baseM = sc.nextDouble();
            System.out.print("Informe a Base menos do Trapézio: ");
            double basem = sc.nextDouble();
            System.out.print("Informe a Altura do Trapézio: ");
            double altura = sc.nextDouble();

            double area = (baseM + basem)*altura/2;
            System.out.println("A área do seu Trapézio: "+area+"m²");
        }
        else if(a == 4){
            System.out.println("=================--================");
            System.out.println("              Círculo");
            System.out.println("=================--================");

            System.out.println("Você possui o Raio ou o Diâmetro?");
            System.out.print("R: ");
            String bola = sc.nextLine();
            if(bola == "Raio"){
                System.out.print("Informe o valor do Raio: ");
                double raio = sc.nextDouble();

                double area = raio * 3.14159;
                System.out.print("A área do seu Círculo: "+area+"m²");
            }
            else if(bola == "Diametro"){
                System.out.print("Informe o valor do Diametro para eu calcular o Raio: ");
                double diametro = sc.nextDouble();

                double raio = diametro / 2;
                System.out.println("O seu raio: "+raio);
                double area = raio * 3.14159;
                System.out.println("A area usando o raio: "+area+"m²");

            }
        }
    }
}
