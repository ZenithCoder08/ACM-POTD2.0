import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        StringBuilder sb = new StringBuilder();

        for (int i = 1; i <= n; i++) {
            if (i % 2 == 1) {
                sb.append("I hate");
            } else {
                sb.append("I love");
            }

            if (i < n) {
                sb.append(" that ");
            } else {
                sb.append(" it");
            }
        }

        System.out.println(sb.toString());
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/12-11-2026.png
