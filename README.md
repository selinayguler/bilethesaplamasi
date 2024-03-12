# bilethesaplamasi
package patika;
import java.util.Scanner;

public class ucakbileti {

    public static void main(String[] args) {
        int yas , yolculukTuru;
        double mesafe,ilkTutar,ikinciTutar,sonTutar;


        Scanner input = new Scanner(System.in);
        System.out.print("Mesafeyi km türünden giriniz:");
        mesafe = input.nextDouble();
        System.out.print("Yolculuk türünüzü giriniz:");
        yolculukTuru = input.nextInt();
        System.out.print("Yaşınızı giriniz:");
        yas = input.nextInt();



        ilkTutar= mesafe*0.10;
        System.out.println("Mesafeye bağlı tutarınız:" + ilkTutar);
        if (yolculukTuru == 2) {
            ikinciTutar=ilkTutar*0.20;

        } else {
            ikinciTutar=ilkTutar;

        }
        System.out.println("Yolculuk türüne bağlı tutarınız: " + ikinciTutar);
         if (yas<12) {
            sonTutar = ikinciTutar*0.50;
            System.out.println("Biletinizin son tutar : " + sonTutar);
        } 
        else if (yas>=12 && yas<=24) { 
            sonTutar = ikinciTutar*0.10;
            System.out.println("Biletinizin son tutarı : " +sonTutar);
        }
        else if (yas>65) { 
            sonTutar = ikinciTutar*0.30;
            System.out.println("Biletinizin son tutarı : " + sonTutar);

        }
        else { 
            System.out.println("Biletinizin son tutarı : " +ikinciTutar);
        }
    }
}

