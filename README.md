# Write-a-program-to-calculate-the-sum-of-the-digits-of-any-integer.-For-example-Number-8545604-has-t
Write a program to calculate the sum of the digits of any integer. For example: Number 8545604 has the sum of digits: 8+5+4+5+6+0+4= 32.
package bai03;
 
import java.util.Scanner;
 
public class Main {
 
    
    public static int nhap(){
        Scanner input= new Scanner(System.in);
        boolean check= false;
        int n=0;
        while(!check){
            System.out.print(" ");
            try{
                n= input.nextInt();
                check= true;
            }catch(Exception e){
                System.out.println("Ban phai nhap so! hay nhap lai...");
                input.nextLine();
            }
        }
        return (n);
    }
    public static int tinhTong(long i){
        int sum=0;
        long n;
        while(i!=0){
            n= i%10;
            sum+= n;
            i/=10;
        }
        return (sum);
    }
    public static void main(String[] args){
                System.out.print("Nhap n");
        int n= nhap();
        System.out.println("Tong cua so "+n+" = " +tinhTong(n));
    }
 
}
