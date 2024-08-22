package notas;


public class NOTAS {

 
    public static void main(String[] args) {
       

        double[] notas = {2.5, 3.7, 4.0, 2.8, 3.2, 3.9, 4.5, 1.8, 2.9, 3.3, 3.6, 4.1, 2.7, 3.0, 4.2};

        // Mayor nota
        double mayorNota = notas[0];
        for (double nota : notas) {
            if (nota > mayorNota) {
                mayorNota = nota;
            }
        }

        // Porcentaje de alumnos que aprobaron con nota superior a 3.0
        int countAprobados = 0;
        for (double nota : notas) {
            if (nota > 3.0) {
                countAprobados++;
            }
        }
        double porcentajeAprobados = (countAprobados / (double) notas.length) * 100;

        // Promedio de las notas
        double sumaNotas = 0;
        for (double nota : notas) {
            sumaNotas += nota;
        }
        double promedioNotas = sumaNotas / notas.length;

        // Posición de la menor nota
        double menorNota = notas[0];
        int posicionMenorNota = 0;
        for (int i = 1; i < notas.length; i++) {
            if (notas[i] < menorNota) {
                menorNota = notas[i];
                posicionMenorNota = i;
            }
        }

        // Resultados
        System.out.println("La mayor nota es: " + mayorNota);
        System.out.println("El porcentaje de alumnos que aprobaron con nota superior a 3.0 es: " + porcentajeAprobados + "%");
        System.out.println("El promedio de las notas es: " + promedioNotas);
        System.out.println("La posición de la menor nota es: " + posicionMenorNota);
    }
}

    
