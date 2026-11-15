import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int[] sticks = new int[4];
        for (int i = 0; i < 4; i++) {
            sticks[i] = Integer.parseInt(st.nextToken());
        }

        Arrays.sort(sticks);

        // Check if a non-degenerate triangle can be formed
        if (sticks[0] + sticks[1] > sticks[2] || sticks[1] + sticks[2] > sticks[3]) {
            System.out.println("TRIANGLE");
        } 
        // Check if a degenerate triangle (segment) can be formed
        else if (sticks[0] + sticks[1] == sticks[2] || sticks[1] + sticks[2] == sticks[3]) {
            System.out.println("SEGMENT");
        } 
        // Otherwise, no triangle is possible
        else {
            System.out.println("IMPOSSIBLE");
        }
    }
}


URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/15-11-2026.png
