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
        int k = Integer.parseInt(st.nextToken());

        int[] a = new int[n];
        st = new StringTokenizer(br.readLine());
        for (int i = 0; i < n; i++) {
            a[i] = Integer.parseInt(st.nextToken());
        }

        if (k > n) {
            System.out.println(-1);
            return;
        }

        Arrays.sort(a);

        // The k-th largest element in ascending sorted array is at index (n - k)
        int coord = a[n - k];
        System.out.println(coord + " " + 0);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/24-11-2026.png
