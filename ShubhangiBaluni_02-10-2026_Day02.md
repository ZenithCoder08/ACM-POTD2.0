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

        String[] flag = new String[n];
        for (int i = 0; i < n; i++) {
            flag[i] = br.readLine();
        }

        boolean isValid = true;

        for (int i = 0; i < n; i++) {
            char rowColor = flag[i].charAt(0);

            // Condition 1: Check if all cells in this row have the same color
            for (int j = 1; j < m; j++) {
                if (flag[i].charAt(j) != rowColor) {
                    isValid = false;
                    break;
                }
            }

            if (!isValid) break;

            // Condition 2: Check if adjacent rows have different colors
            if (i > 0 && rowColor == flag[i - 1].charAt(0)) {
                isValid = false;
                break;
            }
        }

        if (isValid) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/02-10-2026.png
