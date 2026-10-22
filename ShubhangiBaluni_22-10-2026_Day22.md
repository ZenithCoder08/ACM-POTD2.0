import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        // Maximum Coders is ceil(n * n / 2)
        int maxCoders = (n * n + 1) / 2;

        StringBuilder sb = new StringBuilder();
        sb.append(maxCoders).append("\n");

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if ((i + j) % 2 == 0) {
                    sb.append('C');
                } else {
                    sb.append('.');
                }
            }
            sb.append("\n");
        }

        System.out.print(sb);
    }


}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/22-10-2026.png
