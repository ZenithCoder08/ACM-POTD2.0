import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        int a = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());

        int[] recipient = new int[n + 1];

        // Arthur's preferred apples
        st = new StringTokenizer(br.readLine());
        for (int i = 0; i < a; i++) {
            int apple = Integer.parseInt(st.nextToken());
            recipient[apple] = 1;
        }

        // Alexander's preferred apples
        st = new StringTokenizer(br.readLine());
        for (int i = 0; i < b; i++) {
            int apple = Integer.parseInt(st.nextToken());
            if (recipient[apple] == 0) {
                recipient[apple] = 2;
            }
        }

        StringBuilder sb = new StringBuilder();
        for (int i = 1; i <= n; i++) {
            sb.append(recipient[i]).append(i == n ? "" : " ");
        }

        System.out.println(sb.toString());
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/25-10-2026.png
