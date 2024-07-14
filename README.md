import java.util.Scanner;
public class Main {
    public static int findFirstIndex(int[] arr, int currentIndex, int M) {
        if (currentIndex == arr.length) {
            return -1;
        }
        if (arr[currentIndex] == M) {
            return currentIndex;
        }
        return findFirstIndex(arr, currentIndex + 1, M);
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt();
        int[] arr = new int[N];
        for (int i = 0; i < N; i++) {
            arr[i] = scanner.nextInt();
        }
        int M = scanner.nextInt();
        int result = findFirstIndex(arr, 0, M);
        System.out.println(result);
    }
}

