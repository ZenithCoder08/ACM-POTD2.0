import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.Arrays;

public class Main {
    static class Container implements Comparable<Container> {
        long boxes;
        long matchesPerBox;

        Container(long boxes, long matchesPerBox) {
            this.boxes = boxes;
            this.matchesPerBox = matchesPerBox;
        }

        @Override
        public int compareTo(Container other) {
            // Sort in descending order of matchesPerBox
            return Long.compare(other.matchesPerBox, this.matchesPerBox);
        }
    }

    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        long n = Long.parseLong(st.nextToken());
        int m = Integer.parseInt(st.nextToken());

        Container[] containers = new Container[m];
        for (int i = 0; i < m; i++) {
            st = new StringTokenizer(br.readLine());
            long a = Long.parseLong(st.nextToken());
            long b = Long.parseLong(st.nextToken());
            containers[i] = new Container(a, b);
        }

        Arrays.sort(containers);

        long remainingCapacity = n;
        long totalMatches = 0;

        for (int i = 0; i < m && remainingCapacity > 0; i++) {
            long take = Math.min(remainingCapacity, containers[i].boxes);
            totalMatches += take * containers[i].matchesPerBox;
            remainingCapacity -= take;
        }

        System.out.println(totalMatches);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/17-11-2026.png
