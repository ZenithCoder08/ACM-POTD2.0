import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String s = br.readLine().trim();

        int consecutiveCount = 1;
        boolean isDangerous = false;

        for (int i = 1; i < s.length(); i++) {
            if (s.charAt(i) == s.charAt(i - 1)) {
                consecutiveCount++;
                if (consecutiveCount >= 7) {
                    isDangerous = true;
                    break;
                }
            } else {
                consecutiveCount = 1;
            }
        }

        System.out.println(isDangerous ? "YES" : "NO");
    }
}


URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/22-11-2026.png
