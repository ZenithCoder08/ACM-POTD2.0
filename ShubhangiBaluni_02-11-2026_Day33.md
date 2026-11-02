import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        long n = Long.parseLong(br.readLine().trim());

        if (n % 2 == 0) {
            System.out.println(n / 2);
        } else {
            System.out.println(-((n + 1) / 2));
        }
    }
}

URL : 
