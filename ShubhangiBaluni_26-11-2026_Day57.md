import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int[][] presses = new int[3][3];

        for (int r = 0; r < 3; r++) {
            StringTokenizer st = new StringTokenizer(br.readLine());
            for (int c = 0; c < 3; c++) {
                presses[r][c] = Integer.parseInt(st.nextToken());
            }
        }

        // Direction vectors for self, up, down, left, right
        int[] dr = {0, -1, 1, 0, 0};
        int[] dc = {0, 0, 0, -1, 1};

        StringBuilder sb = new StringBuilder();
        for (int r = 0; r < 3; r++) {
            for (int c = 0; c < 3; c++) {
                int totalToggles = 0;
                for (int d = 0; d < 5; d++) {
                    int nr = r + dr[d];
                    int nc = c + dc[d];
                    if (nr >= 0 && nr < 3 && nc >= 0 && nc < 3) {
                        totalToggles += presses[nr][nc];
                    }
                }
                // Starts ON (1): even toggles -> 1, odd toggles -> 0
                sb.append(totalToggles % 2 == 0 ? '1' : '0');
            }
            sb.append('\n');
        }

        System.out.print(sb);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/26-11-2026.png
