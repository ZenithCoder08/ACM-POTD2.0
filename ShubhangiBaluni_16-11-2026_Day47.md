import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        long d = Long.parseLong(st.nextToken());

        st = new StringTokenizer(br.readLine());
        long prev = Long.parseLong(st.nextToken());
        long totalMoves = 0;

        for (int i = 1; i < n; i++) {
            long curr = Long.parseLong(st.nextToken());
            if (curr <= prev) {
                long diff = prev - curr;
                long moves = (diff / d) + 1;
                totalMoves += moves;
                curr += moves * d;
            }
            prev = curr;
        }

        System.out.println(totalMoves);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/16-11-2026.png
