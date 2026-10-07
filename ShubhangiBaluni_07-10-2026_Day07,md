import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(br.readLine().trim());

        int[] d = new int[n - 1];
        StringTokenizer st = new StringTokenizer(br.readLine());
        for (int i = 0; i < n - 1; i++) {
            d[i] = Integer.parseInt(st.nextToken());
        }

        st = new StringTokenizer(br.readLine());
        int a = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());

        // Sum the years from rank a to rank b
        int totalYears = 0;
        for (int i = a - 1; i < b - 1; i++) {
            totalYears += d[i];
        }

        System.out.println(totalYears);
    }

   URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/07-10-2026.png
URL : }
