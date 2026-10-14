import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        String s1 = br.readLine().trim();
        String s2 = br.readLine().trim();

        int cmp = s1.compareToIgnoreCase(s2);

        if (cmp < 0) {
            System.out.println("-1");
        } else if (cmp > 0) {
            System.out.println("1");
        } else {
            System.out.println("0");
        }
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/13-10-2026.png
