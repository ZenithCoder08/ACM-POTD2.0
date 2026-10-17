import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.HashSet;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        HashSet<Integer> uniqueColors = new HashSet<>();
        for (int i = 0; i < 4; i++) {
            uniqueColors.add(Integer.parseInt(st.nextToken()));
        }

        int toBuy = 4 - uniqueColors.size();
        System.out.println(toBuy);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/17-10-2026.png
