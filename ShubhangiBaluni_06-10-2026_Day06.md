import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        int n = Integer.parseInt(br.readLine().trim());
        int[] a = new int[n];
        
        StringTokenizer st = new StringTokenizer(br.readLine());
        for (int i = 0; i < n; i++) {
            a[i] = Integer.parseInt(st.nextToken());
        }

        int minDiff = Integer.MAX_VALUE;
        int ans1 = 1;
        int ans2 = 2;

        for (int i = 0; i < n; i++) {
            int next = (i + 1) % n;
            int diff = Math.abs(a[i] - a[next]);

            if (diff < minDiff) {
                minDiff = diff;
                ans1 = i + 1;       // 1-based index
                ans2 = next + 1;    // 1-based index
            }
        }

        System.out.println(ans1 + " " + ans2);
    }

 
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/06-10-2026.png
