import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.HashSet;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        int n = Integer.parseInt(br.readLine().trim());
        HashSet<Integer> passedLevels = new HashSet<>();

        // Read Little X's levels
        StringTokenizer st = new StringTokenizer(br.readLine());
        int p = Integer.parseInt(st.nextToken());
        for (int i = 0; i < p; i++) {
            passedLevels.add(Integer.parseInt(st.nextToken()));
        }

        // Read Little Y's levels
        st = new StringTokenizer(br.readLine());
        int q = Integer.parseInt(st.nextToken());
        for (int i = 0; i < q; i++) {
            passedLevels.add(Integer.parseInt(st.nextToken()));
        }

        if (passedLevels.size() == n) {
            System.out.println("I become the guy.");
        } else {
            System.out.println("Oh, my keyboard!");
        }
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/31-10-2026.png
