import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String s = br.readLine();

        if (s == null) return;

        s = s.trim();

        if (s.length() < 5) {
            System.out.println("Too weak");
            return;
        }

        boolean hasUpper = false;
        boolean hasLower = false;
        boolean hasDigit = false;

        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            if (Character.isUpperCase(c)) {
                hasUpper = true;
            } else if (Character.isLowerCase(c)) {
                hasLower = true;
            } else if (Character.isDigit(c)) {
                hasDigit = true;
            }
        }

        if (hasUpper && hasLower && hasDigit) {
            System.out.println("Correct");
        } else {
            System.out.println("Too weak");
        }
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/24-10-2026.png
