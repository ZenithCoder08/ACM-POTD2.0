import java.io.InputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        FastScanner fs = new FastScanner(System.in);
        int n = fs.nextInt();

        long totalSum = (long) n * (n + 1) / 2;
        long watchedSum = 0;

        for (int i = 0; i < n - 1; i++) {
            watchedSum += fs.nextInt();
        }

        System.out.println(totalSum - watchedSum);
    }

    // Fast integer reader for large inputs up to 10^5 elements
    static class FastScanner {
        private final InputStream in;
        private final byte[] buffer = new byte[32768];
        private int head = 0;
        private int tail = 0;

        public FastScanner(InputStream in) {
            this.in = in;
        }

        private int read() throws IOException {
            if (head >= tail) {
                head = 0;
                tail = in.read(buffer, 0, buffer.length);
                if (tail <= 0) return -1;
            }
            return buffer[head++];
        }

        public int nextInt() throws IOException {
            int c = read();
            while (c <= ' ' && c != -1) {
                c = read();
            }
            int res = 0;
            while (c > ' ') {
                if (c >= '0' && c <= '9') {
                    res = res * 10 + (c - '0');
                }
                c = read();
            }
            return res;
        }
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/27-10-2026.png
