import java.util.Scanner;
import java.util.Random;

public class PiedraPapelTijeras {

    public static void main(String[] args) {
        // Crear escáner para entrada de usuario y random para elección de la computadora
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        // Opciones del juego
        String[] opciones = {"Piedra", "Papel", "Tijeras"};

        // Pedir al usuario que ingrese su elección
        System.out.println("Elige una opción (0: Piedra, 1: Papel, 2: Tijeras): ");
        int eleccionUsuario = scanner.nextInt();

        // Validar la elección del usuario
        if (eleccionUsuario < 0 || eleccionUsuario > 2) {
            System.out.println("Elección no válida, debe ser 0, 1 o 2.");
            return;
        }

        // Elección de la computadora
        int eleccionComputadora = random.nextInt(3);

        // Mostrar las elecciones
        System.out.println("Tú elegiste: " + opciones[eleccionUsuario]);
        System.out.println("La computadora eligió: " + opciones[eleccionComputadora]);

        // Comparar las elecciones y determinar el ganador
        if (eleccionUsuario == eleccionComputadora) {
            System.out.println("Es un empate!");
        } else if ((eleccionUsuario == 0 && eleccionComputadora == 2) || // Piedra vs Tijeras
                   (eleccionUsuario == 1 && eleccionComputadora == 0) || // Papel vs Piedra
                   (eleccionUsuario == 2 && eleccionComputadora == 1)) {  // Tijeras vs Papel
            System.out.println("¡Ganaste!");
        } else {
            System.out.println("¡La computadora gana!");
        }

        // Cerrar el escáner
        scanner.close();
    }
}
