import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        int s = Integer.parseInt(st.nextToken());

        st = new StringTokenizer(br.readLine());
        int totalSum = 0;
        int maxMug = 0;

        for (int i = 0; i < n; i++) {
            int a = Integer.parseInt(st.nextToken());
            totalSum += a;
            if (a > maxMug) {
                maxMug = a;
            }
        }

        // Sum of the (n - 1) smallest mugs
        int minPoured = totalSum - maxMug;

        if (minPoured <= s) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/26-10-2026.png
