import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String s = br.readLine();

        if (s == null || s.isEmpty()) {
            return;
        }

        StringBuilder sb = new StringBuilder();
        int n = s.length();
        int i = 0;

        while (i < n) {
            if (s.charAt(i) == '.') {
                sb.append('0');
                i++;
            } else if (s.charAt(i) == '-') {
                if (s.charAt(i + 1) == '.') {
                    sb.append('1');
                } else {
                    sb.append('2');
                }
                i += 2;
            }
        }

        System.out.println(sb.toString());
    }

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/05-10-2026.png
}
