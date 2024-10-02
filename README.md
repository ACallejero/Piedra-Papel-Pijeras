public class Main {

    public static void main(String[] args) {
        int Tijeras = 0;
        int Papel = 1;
        int Piedra = 2;
        
        int maquina1 = (int)(Math.random() * 3);
        int maquina2 = (int)(Math.random() * 3);
        
        if (maquina1 == Tijeras && maquina2 == Tijeras) {
            System.out.println("Tijeras, Tijeras empate");
        } else if (maquina1 == Tijeras && maquina2 == Papel) {
            System.out.println("Tijeras, Papel gana maquina2");
        } else if (maquina1 == Tijeras && maquina2 == Piedra) {
            System.out.println("Tijeras, Piedra gana maquina1");
        } else if (maquina1 == Papel && maquina2 == Tijeras) {
            System.out.println("Papel, Tijeras gana maquina2");
        } else if (maquina1 == Papel && maquina2 == Papel) {
            System.out.println("Papel, Papel empate");
        } else if (maquina1 == Papel && maquina2 == Piedra) {
            System.out.println("Papel, Piedra gana maquina1");
        } else if (maquina1 == Piedra && maquina2 == Tijeras) {
            System.out.println("Piedra, Tijeras gana maquina2");
        } else if (maquina1 == Piedra && maquina2 == Papel) {
            System.out.println("Piedra, Papel gana maquina1");
        } else {
            System.out.println("Piedra, Piedra empate");
        }
    }
}
