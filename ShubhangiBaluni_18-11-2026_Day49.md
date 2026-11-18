import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        int[] primeDivisorsCount = new int[n + 1];

        for (int i = 2; i <= n; i++) {
            // If primeDivisorsCount[i] == 0, i is a prime number
            if (primeDivisorsCount[i] == 0) {
                for (int j = i; j <= n; j += i) {
                    primeDivisorsCount[j]++;
                }
            }
        }

        int almostPrimeCount = 0;
        for (int i = 1; i <= n; i++) {
            if (primeDivisorsCount[i] == 2) {
                almostPrimeCount++;
            }
        }

        System.out.println(almostPrimeCount);
    }
}

URL : 
