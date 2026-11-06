import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int a = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());

        int fashionableDays = Math.min(a, b);
        int sameDays = Math.abs(a - b) / 2;

        System.out.println(fashionableDays + " " + sameDays);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/06-11-2026.png
