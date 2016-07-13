# China-Soft-Technical-Quest
using System;
using System.Text;
namespace IntToRoman
{
   Class Roman
   {
       static void Main()
       {
          ToRoman(2016);
       }
       
       static string ToRoman(int number)
       {
            StringBuilder sb=new StringBuilder
            int remain=number;
            while (remain>0)
            {
            if(number<0 || number>3999) throw new ArgumentOutOfRangeException("Insert value between 1 and 3999.");
            if(number<1) return string.Empty;
            if(number>=1000) {sb.Append("M");remain-=1000;}
            if(number>=900) {sb.Append("CM");remain-=900;}
            if(number>=500) {sb.Append("D");remain-=500;}
            if(number>=400) {sb.Append("CD");remain-=400;}
            if(number>=100) {sb.Append("C");remain-=100;}
            if(number>=90) {sb.Append("XC");remain-=90;}
            if(number>=50) {sb.Append("L");remain-=50;}
            if(number>=40) {sb.Append("XL");remain-=40;}
            if(number>=10) {sb.Append("X");remain-=10;}
            if(number>=9) {sb.Append("IX");remain-=9;}
            if(number>=5) {sb.Append("V");remain-=5;}
            if(number>=4) {sb.Append("IV");remain-=4;}
            if(number>=1) {sb.Append("I");remain-=1;}
            
            
            }
            
            return sb.ToString();
       }
   }
}
