import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        long n = Long.parseLong(st.nextToken());
        long k = Long.parseLong(st.nextToken());

        long x = n + (k - n % k);

        System.out.println(x);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/09-11-2026.png
