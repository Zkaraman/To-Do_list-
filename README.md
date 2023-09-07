# To-Do_list-
#TO-DO liste
import java.util.Scanner;
public class ToList {
    private String gun;
    private String [] gorevler;
    private int gorevSayi;


     public ToList(int gorevSayisi, String gun) {
         this.gun = gun;
         this.gorevSayi = gorevSayisi;
         this.gorevler = new String[gorevSayisi];
     }
     public void  gorevleriEkleme(Scanner scanner) {
         for (int i = 0; i < gorevSayi; i++) {
             System.out.println(i + 1 + " . görev ");
             gorevler[i] = scanner.next();
         }
     }
     public void gorevleriListele(){
         System.out.println(gun + "  gunun gorevi şunlar");
         for (int i = 0; i < gorevSayi; i++) {

             System.out.print(gorevler[i]+ " ,  " );
         }
}}



public class Main {
    public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    System.out.println("gun giriniz: ");
    String gun = scanner.next();
    System.out.println("kac gorev girilecek");

        int gorevSayiyi = scanner.nextInt();
        ToList toList= new ToList(gorevSayiyi,gun );
        toList.gorevleriEkleme(sc);
        toList.gorevleriListele();
        scanner.close(); }}
