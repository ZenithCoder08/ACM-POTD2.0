import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.HashSet;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();

        if (line == null) return;

        HashSet<Character> distinctLetters = new HashSet<>();

        for (int i = 0; i < line.length(); i++) {
            char c = line.charAt(i);
            if (c >= 'a' && c <= 'z') {
                distinctLetters.add(c);
            }
        }

        System.out.println(distinctLetters.size());
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/28-10-2026.png
