import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        int m = Integer.parseInt(st.nextToken());

        String[] grid = new String[n];
        for (int i = 0; i < n; i++) {
            grid[i] = br.readLine();
        }

        // Initialize bounding box coordinates
        int minRow = n, maxRow = -1;
        int minCol = m, maxCol = -1;

        // Find the bounding box containing all '*'
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                if (grid[i].charAt(j) == '*') {
                    if (i < minRow) minRow = i;
                    if (i > maxRow) maxRow = i;
                    if (j < minCol) minCol = j;
                    if (j > maxCol) maxCol = j;
                }
            }
        }

        // Output the cropped rectangle
        StringBuilder sb = new StringBuilder();
        for (int i = minRow; i <= maxRow; i++) {
            sb.append(grid[i].substring(minCol, maxCol + 1)).append("\n");
        }

        System.out.print(sb);
    }


}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/01-10-2026.png
