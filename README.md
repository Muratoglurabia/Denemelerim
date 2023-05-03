# Denemelerim
package ATM;

import java.util.Scanner;

public class AtmUygulaması {

	public static void main(String[] args) {
		// strıng ıle cekme bak
        
        int bakiye = 1000;
        int miktar;
		Scanner reader = new Scanner (System.in);
		System.out.println("Hosgeldiniz. Yapmak istediginiz islemi seciniz");
		System.out.println("1 : Bakiye goruntule ");
		System.out.println("2 : Para cekme ");
		System.out.println("3 : Para yatirma ");
		System.out.println("4 : cikis yapiliyor ");
		int islem = reader.nextInt();
		
		switch (islem) {
		case 1 : System.out.println("Bakiyeniz :" + bakiye +"tldir");
		break;
	    case 2 : System.out.println("Ne kadar cekmek istersiniz?");
	    miktar = reader.nextInt();
	    bakiye = bakiye- miktar;
	    if(miktar>1000) {
	    	System.out.println("Bakiye yetersiz");
	    }
	    else {
	    	if (miktar<1000)
	    	 System.out.println("Bakiyeniz :" + bakiye +"tldir");
	     }
	
	    break;
	    case 3 : System.out.println("Ne kadar yatirmak istersiniz?");
	    miktar = reader.nextInt();
	    bakiye = bakiye + miktar;
	    System.out.println("Bakiyeniz :" + bakiye +"tldir");
	   
		break;
	    case 4 : System.out.println("Cikis yapiliyor...");
		break; 
		default : System.out.println("Gecersiz islem yaptiniz");
		}
		reader.close();
		
	}
		

}

