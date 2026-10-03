import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.TreeSet;
import java.util.Iterator;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        int n = Integer.parseInt(br.readLine().trim());
        StringTokenizer st = new StringTokenizer(br.readLine());
        
        // TreeSet keeps elements unique and sorted in ascending order
        TreeSet<Integer> distinctSorted = new TreeSet<>();
        for (int i = 0; i < n; i++) {
            distinctSorted.add(Integer.parseInt(st.nextToken()));
        }
        
        // If there are fewer than 2 distinct elements, second order statistic does not exist
        if (distinctSorted.size() < 2) {
            System.out.println("NO");
        } else {
            Iterator<Integer> it = distinctSorted.iterator();
            it.next(); // Skip the minimum (first element)
            System.out.println(it.next()); // The second minimum
        }
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/03-10-2026.png
