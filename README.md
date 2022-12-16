package odev_heap;

import java.util.Arrays;
import java.util.Scanner;

public class Odev_Heap {

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        int hdizi[] = new int[4];// 4 olsun  :{
        System.out.println("Lütfen sayıları girininiz");
        for (int i = 0; i < hdizi.length; i++) {
            System.out.println((i + 1) + ".sayıyı girdiniz");
            hdizi[i] = s.nextInt();

        }
        System.out.println("Girilen dizi");
        System.out.println(Arrays.toString(hdizi));

        int tmp = 0;
       
        
        
        for(int a=0; a<hdizi.length ;a++){
            
            if (hdizi[a] > hdizi[3 * a + 1]) {
                tmp = hdizi[a];
                hdizi[a] = hdizi[3 * a + 1];
                hdizi[3 * a + 1] = tmp;

            } else if (hdizi[a] > hdizi[3 * a + 2]) {
                tmp = hdizi[a];
                hdizi[a] = hdizi[3 * a + 2];
                hdizi[3 * a + 2] = tmp;

            }else if(hdizi[a]>hdizi[3*a+3]){
                tmp = hdizi[a];
                hdizi[a] = hdizi[3 * a + 3];
                hdizi[3 * a + 3] = tmp;
        }
                
        }
        
        System.out.println(Arrays.toString(hdizi)); 
    }}
// 02190201046
