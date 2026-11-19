import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        int m = Integer.parseInt(st.nextToken());

        int[] prices = new int[n];
        st = new StringTokenizer(br.readLine());
        for (int i = 0; i < n; i++) {
            prices[i] = Integer.parseInt(st.nextToken());
        }

        Arrays.sort(prices);

        int maxEarnings = 0;
        for (int i = 0; i < m; i++) {
            if (prices[i] < 0) {
                maxEarnings += -prices[i];
            } else {
                break;
            }
        }

        System.out.println(maxEarnings);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/19-11-2026.png
