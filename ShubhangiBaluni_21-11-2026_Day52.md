import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        int[] count = new int[4];
        StringTokenizer st = new StringTokenizer(br.readLine());

        for (int i = 0; i < n; i++) {
            int val = Integer.parseInt(st.nextToken());
            count[val]++;
        }

        int maxFreq = Math.max(count[1], Math.max(count[2], count[3]));
        System.out.println(n - maxFreq);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/21-11-2026.png
