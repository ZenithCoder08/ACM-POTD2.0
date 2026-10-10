import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        int k = 1;
        boolean isTriangular = false;

        while (true) {
            int triangular = k * (k + 1) / 2;
            if (triangular == n) {
                isTriangular = true;
                break;
            } else if (triangular > n) {
                break;
            }
            k++;
        }

        if (isTriangular) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
    }

}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/10-10-2026.png
