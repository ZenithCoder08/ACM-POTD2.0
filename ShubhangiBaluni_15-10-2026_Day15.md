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

        int ansRow = 0;
        int ansCol = 0;

        for (int i = 1; i <= n; i++) {
            String row = br.readLine();
            for (int j = 1; j <= m; j++) {
                if (row.charAt(j - 1) == '*') {
                    ansRow ^= i;
                    ansCol ^= j;
                }
            }
        }

        System.out.println(ansRow + " " + ansCol);
    }


  URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/15-10-2026.png


URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/15-10-2026.png
}
