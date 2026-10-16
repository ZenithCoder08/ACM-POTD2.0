import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        int m = Integer.parseInt(st.nextToken());

        int count = 0;

        // Since a^2 <= n and a >= 0:
        for (int a = 0; a * a <= n; a++) {
            int b = n - a * a;
            if (a + b * b == m) {
                count++;
            }
        }

        System.out.println(count);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/16-10-2026.png
