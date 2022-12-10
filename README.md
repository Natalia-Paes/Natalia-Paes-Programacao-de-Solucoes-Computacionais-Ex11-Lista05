# Natalia-Paes-Programacao-de-Solucoes-Computacionais-Ex11-Lista05
Data com mês por extenso.
import java.util.Scanner;

public class Ex11 {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        System.out.println("Informe uma data: [DD/MM/AAAA] ");
        String date = sc.next();
        sc.close();
        System.out.println(convertDate(date));
    }

    public static String convertDate(String dateCompleted) {
        String[] months = { "Janeiro", "Fevereiro", "Março", "Abril", "Maio", "Junho", "Julho", "Agosto", "Setembro",
                "Outubro", "Novembro", "Dezembro" };
        String[] arrayDate = dateCompleted.split("/");
        int indexMonth = Integer.parseInt(arrayDate[1]);
        arrayDate[1] = months[indexMonth - 1];
        String dateFormat = String.join(" de ", arrayDate);
        return "A data informada é " + dateFormat + ".";
    }
}
