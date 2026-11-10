import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;
import java.util.Arrays;

public class Main {
    static class Card implements Comparable<Card> {
        int val;
        int id;

        Card(int val, int id) {
            this.val = val;
            this.id = id;
        }

        @Override
        public int compareTo(Card other) {
            return Integer.compare(this.val, other.val);
        }
    }

    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine().trim());

        Card[] cards = new Card[n];
        StringTokenizer st = new StringTokenizer(br.readLine());

        for (int i = 0; i < n; i++) {
            cards[i] = new Card(Integer.parseInt(st.nextToken()), i + 1);
        }

        Arrays.sort(cards);

        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < n / 2; i++) {
            sb.append(cards[i].id).append(" ").append(cards[n - 1 - i].id).append("\n");
        }

        System.out.print(sb);
    }
}


URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/10-11-2026.png
