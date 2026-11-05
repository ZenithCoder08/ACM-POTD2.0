import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        long k = Long.parseLong(st.nextToken());
        long n = Long.parseLong(st.nextToken());
        long w = Long.parseLong(st.nextToken());

        long totalCost = k * w * (w + 1) / 2;
        long borrow = Math.max(0L, totalCost - n);

        System.out.println(borrow);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/05-11-2026.png
