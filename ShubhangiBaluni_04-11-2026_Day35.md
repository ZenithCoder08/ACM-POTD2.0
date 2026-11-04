import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        int n = Integer.parseInt(br.readLine().trim());
        String s = br.readLine();

        if (n < 26) {
            System.out.println("NO");
            return;
        }

        boolean[] seen = new boolean[26];
        int distinctCount = 0;

        for (int i = 0; i < n; i++) {
            char c = Character.toLowerCase(s.charAt(i));
            int idx = c - 'a';

            if (!seen[idx]) {
                seen[idx] = true;
                distinctCount++;
                if (distinctCount == 26) {
                    break;
                }
            }
        }

        if (distinctCount == 26) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
    }
}


URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/04-11-2026.png
