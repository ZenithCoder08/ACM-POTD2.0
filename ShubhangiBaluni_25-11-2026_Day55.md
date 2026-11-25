import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        StringBuilder sb = new StringBuilder();

        for (int i = 0; i < n; i++) {
            StringTokenizer st = new StringTokenizer(br.readLine());
            long a = Long.parseLong(st.nextToken());
            long b = Long.parseLong(st.nextToken());

            long operations = 0;
            while (a > 0 && b > 0) {
                if (a >= b) {
                    operations += a / b;
                    a %= b;
                } else {
                    operations += b / a;
                    b %= a;
                }
            }

            sb.append(operations).append("\n");
        }

        System.out.print(sb);
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/25-11-2026.png
