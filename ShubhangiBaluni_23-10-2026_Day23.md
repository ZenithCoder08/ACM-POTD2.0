import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        int n = Integer.parseInt(br.readLine().trim());
        StringTokenizer st = new StringTokenizer(br.readLine());

        int maxVal = -1;
        int maxIndex = -1;
        int secondMaxVal = -1;

        for (int i = 1; i <= n; i++) {
            int p = Integer.parseInt(st.nextToken());

            if (p > maxVal) {
                secondMaxVal = maxVal;
                maxVal = p;
                maxIndex = i;
            } else if (p > secondMaxVal) {
                secondMaxVal = p;
            }
        }

        System.out.println(maxIndex + " " + secondMaxVal);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/23-10-2026.png
