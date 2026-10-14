import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        int k = Integer.parseInt(st.nextToken());

        int[] a = new int[n];
        st = new StringTokenizer(br.readLine());
        for (int i = 0; i < n; i++) {
            a[i] = Integer.parseInt(st.nextToken());
        }

        // The benchmark score from the k-th place finisher (1-based index k -> 0-based k-1)
        int benchmarkScore = a[k - 1];

        int advancers = 0;
        for (int i = 0; i < n; i++) {
            if (a[i] >= benchmarkScore && a[i] > 0) {
                advancers++;
            } else {
                break; // Since the list is non-increasing, subsequent scores won't qualify
            }
        }

        System.out.println(advancers);
    }


}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/14-10-2026.png
