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

        String road = br.readLine().trim();

        int consecutiveRocks = 0;
        for (int i = 0; i < n; i++) {
            if (road.charAt(i) == '#') {
                consecutiveRocks++;
                if (consecutiveRocks >= k) {
                    System.out.println("NO");
                    return;
                }
            } else {
                consecutiveRocks = 0;
            }
        }

        System.out.println("YES");
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/27-11-2026.png
