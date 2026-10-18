import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        int n = Integer.parseInt(br.readLine().trim());
        String s = br.readLine().trim();

        int removeCount = 0;
        for (int i = 0; i < n - 1; i++) {
            if (s.charAt(i) == s.charAt(i + 1)) {
                removeCount++;
            }
        }

        System.out.println(removeCount);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/18-10-2026.png
