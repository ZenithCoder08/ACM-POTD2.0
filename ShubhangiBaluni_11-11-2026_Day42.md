import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        StringTokenizer st = new StringTokenizer(br.readLine());
        
        int prev = Integer.parseInt(st.nextToken());
        int currentLength = 1;
        int maxLength = 1;

        for (int i = 1; i < n; i++) {
            int curr = Integer.parseInt(st.nextToken());
            if (curr > prev) {
                currentLength++;
            } else {
                currentLength = 1;
            }
            if (currentLength > maxLength) {
                maxLength = currentLength;
            }
            prev = curr;
        }

        System.out.println(maxLength);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/11-11-2026.png
