# Binary-Search for interers
import java.util.Scanner;
public class SearchingTech {
    public static void main(String[] args) {
        int[] C={1,2,3,4,5,6}; //it is assumed that the sorted array list is given
        int li=0,mi;
        int hi=C.length-1;
        System.out.println("Enter the item you want to search=");
        Scanner sc=new Scanner(System.in);
        int item=sc.nextInt();
        mi=(li+hi)/2;
        while (li<=hi)
        {
            if(C[mi]==item) {
                System.out.println("item is found at index " + mi);
                break;
            }
            else if(C[mi]<item)
                li=mi+1;
            else
                hi=mi-1;
            mi=(li+hi)/2;
        }
        if (li>hi)
            System.out.println("Element not found");

   }
}
