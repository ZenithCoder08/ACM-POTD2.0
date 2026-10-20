import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String word = br.readLine();

        if (word == null || word.isEmpty()) {
            return;
        }

        char firstChar = Character.toUpperCase(word.charAt(0));
        String result = firstChar + word.substring(1);

        System.out.println(result);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD2.0/blob/main/20-10-2026.png
