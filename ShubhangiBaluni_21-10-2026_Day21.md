import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String s = br.readLine();

        if (s == null || s.isEmpty()) return;

        // Split by the '+' symbol (escaped in regex as "\\+")
        String[] numbers = s.split("\\+");

        // Sort the numbers alphabetically/numerically (works identically since all numbers are single digits 1, 2, 3)
        Arrays.sort(numbers);

        // Join sorted numbers back with '+'
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < numbers.length; i++) {
            sb.append(numbers[i]);
            if (i < numbers.length - 1) {
                sb.append("+");
            }
        }

        System.out.println(sb.toString());
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/21-10-2026.png
