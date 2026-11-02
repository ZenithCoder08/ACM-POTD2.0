import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        int height = 0;
        int currentLevelCubes = 0;
        int totalCubesUsed = 0;

        while (true) {
            int nextLevel = height + 1;
            currentLevelCubes += nextLevel;

            if (totalCubesUsed + currentLevelCubes <= n) {
                totalCubesUsed += currentLevelCubes;
                height = nextLevel;
            } else {
                break;
            }
        }

        System.out.println(height);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/03-11-2026.png
