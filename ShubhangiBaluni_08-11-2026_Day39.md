import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        // Read n (up to 2 * 10^18)
        br.readLine();

        // For all n >= 2, the last two digits are always 25
        System.out.println(25);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/08-11-2026.png
