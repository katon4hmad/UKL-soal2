# UKL-soal2
program ini berfungsi untuk menghitung nilai dari uang
package latihanukl1;

import java.util.Scanner;
 
public class soal2 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int[] pecahan = {100000, 50000, 20000, 10000, 5000, 2000, 1000, 500, 200, 100};

        System.out.print("Masukkan jumlah uang: ");
        int uang = input.nextInt();

        System.out.println("\nPecahan yang dibutuhkan:");
        
        for (int p : pecahan) {
            int jumlah = uang / p;    
            if (jumlah > 0) {
                System.out.println("Rp " + p + " : " + jumlah + " lembar/koin");
            }
            uang %= p;                
        }

        if (uang > 0) {
            System.out.println("Sisa yang tidak dapat dipecah: Rp " + uang);
        }
    }
}
