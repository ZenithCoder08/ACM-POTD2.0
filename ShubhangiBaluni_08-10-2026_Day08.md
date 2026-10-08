import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        String s = br.readLine().trim();
        String t = br.readLine().trim();

        String reversedS = new StringBuilder(s).reverse().toString();

        if (reversedS.equals(t)) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/08-10-2026.png
