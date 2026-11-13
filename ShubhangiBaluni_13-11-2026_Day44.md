import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String pos = br.readLine().trim();

        int col = pos.charAt(0) - 'a';
        int row = pos.charAt(1) - '1';

        int validMoves = 0;

        for (int dc = -1; dc <= 1; dc++) {
            for (int dr = -1; dr <= 1; dr++) {
                if (dc == 0 && dr == 0) continue;

                int nextCol = col + dc;
                int nextRow = row + dr;

                if (nextCol >= 0 && nextCol < 8 && nextRow >= 0 && nextRow < 8) {
                    validMoves++;
                }
            }
        }

        System.out.println(validMoves);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/13-11-2026.png
