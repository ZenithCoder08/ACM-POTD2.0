import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        if (n % 2 == 0) {
            System.out.println(4 + " " + (n - 4));
        } else {
            System.out.println(9 + " " + (n - 9));
        }
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/01-11-2026.png
