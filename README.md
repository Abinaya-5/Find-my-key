# Find-my-key

import java.io.*;
import java.util.*;
public class Solution {
        public static int largest(int a,int b,int c){
            if(a>b&&a>c)
                return a;
                else if(b>c)
                    return b;
                else
                    return c;   
        }
        public static int smallest(int a,int b,int c){
            if(a<b&&a<c)
                return a;
            else if(b<c)
                return b;
            else
                return c;        
        }
    public static void main(String[] args){
        Scanner s=new Scanner(System.in);
        int input1=s.nextInt();
        int input2=s.nextInt();
        int input3=s.nextInt();
        String ai=Integer.toString(input1);
        String bi=Integer.toString(input2);
        String ci=Integer.toString(input3);
        char[] a1=ai.toCharArray();
        char[] b1=bi.toCharArray();
        char[] c1=ci.toCharArray();
        String key="";
        key+=smallest(a1[0]-48,b1[0]-48,c1[0]-48);
        key+=largest(a1[1]-48,b1[1]-48,c1[1]-48);
        key+=smallest(a1[2]-48,b1[2]-48,c1[2]-48);
        key+=largest(a1[3]-48,b1[3]-48,c1[3]-48);
        System.out.println(key); 
    }
}
