import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int y = Integer.parseInt(br.readLine().trim());

        while (true) {
            y++;
            int a = y / 1000;
            int b = (y / 100) % 10;
            int c = (y / 10) % 10;
            int d = y % 10;

            if (a != b && a != c && a != d && b != c && b != d && c != d) {
                System.out.println(y);
                break;
            }
        }
    }
}


URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/19-10-2026.png
