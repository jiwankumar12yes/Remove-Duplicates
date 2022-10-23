# Remove-Duplicates
/*Given a string S, remove consecutive duplicates from it recursively.
Input Format :
String S
Output Format :
Output string
Constraints :
1 <= |S| <= 10^3
where |S| represents the length of string
Sample Input 1 :
aabccba
Sample Output 1 :
abcba
Sample Input 2 :
xxxyyyzwwzzz
Sample Output 2 :
xyzwz
*/
package recursion2;
import java.util.*;
public class remove_duplicate {
    
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        String str=s.next();
        System.out.println(Remove(str));
    }
    public static String Remove(String str){
        if(str.length()<=1){
            return str;
        }
        String smallans=Remove(str.substring(1));
        if(str.charAt(0)==str.charAt(1)){
            // smallans=str.charAt(1);
            return smallans;
        }
        else{
            return str.charAt(0)+smallans;
        }
    }
}
