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

        boolean[] turnedOn = new boolean[m + 1];
        int litBulbsCount = 0;

        for (int i = 0; i < n; i++) {
            st = new StringTokenizer(br.readLine());
            int x = Integer.parseInt(st.nextToken());

            for (int j = 0; j < x; j++) {
                int bulb = Integer.parseInt(st.nextToken());
                if (!turnedOn[bulb]) {
                    turnedOn[bulb] = true;
                    litBulbsCount++;
                }
            }
        }

        if (litBulbsCount == m) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/07-11-2026.png
