import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        int mid = n / 2;
        StringBuilder sb = new StringBuilder();

        for (int i = 0; i < n; i++) {
            int dist = Math.abs(i - mid);
            int dCount = n - 2 * dist;

            // Leading stars
            for (int j = 0; j < dist; j++) {
                sb.append('*');
            }
            // Diamond center
            for (int j = 0; j < dCount; j++) {
                sb.append('D');
            }
            // Trailing stars
            for (int j = 0; j < dist; j++) {
                sb.append('*');
            }
            sb.append("\n");
        }

        System.out.print(sb);
    }
}
