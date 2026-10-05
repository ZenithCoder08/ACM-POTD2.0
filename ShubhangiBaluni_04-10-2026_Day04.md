import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        int n = Integer.parseInt(st.nextToken());
        long d = Long.parseLong(st.nextToken());

        long[] a = new long[n];
        st = new StringTokenizer(br.readLine());
        for (int i = 0; i < n; i++) {
            a[i] = Long.parseLong(st.nextToken());
        }

        Arrays.sort(a);

        long count = 0;
        int right = 0;

        // Two-pointer window: for each 'left', find all 'right' such that a[right] - a[left] <= d
        for (int left = 0; left < n; left++) {
            while (right < n && a[right] - a[left] <= d) {
                right++;
            }
            // All elements from (left + 1) to (right - 1) form valid pairs with 'left'
            count += (right - left - 1);
        }

        // Since (i, j) and (j, i) are distinct, multiply by 2
        System.out.println(count * 2);
    }

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/04-10-2026.png
}
