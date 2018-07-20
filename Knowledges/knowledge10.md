## Why there is no pass by reference in Java

တခ်ိဳ. Java programmer ေတြ blog ေတြမွာ Java မွာ parameter passing မွာ Object ေတြသည္ pass by reference နဲ.သြားတယ္လုိ.ေရးၾကပါတယ္။ တကယ္ေတာ့ Java မွာ pass by value ပဲရိွပါတယ္။ အေသးစိတ္သိခ်င္ရင္ေတာ့ JLS(Java Language Specification) ကုိသာ နားလည္ေအာင္ဖတ္ၾကည့္ပါ။

ဘာလုိ. Java မွာ pass by value ပဲရိွတာလဲ။ Pass by reference မရိွဘူးလား။ ဒါဆုိရင္ method တခုကို parameter အေနနဲ.ေပးလိုက္တဲ့ object ေတြရဲ. data ကုိၿပင္ရင္ method အၿပင္ကေန effect ၿဖစ္တယ္ေပါ့။ ဒါမ်ိဳးဆုိ pass by reference မဟုတ္ဘူးလားေပ့ါ။ ဥပမာ ဒီ code ေပါ့။

class Data{
int counter;
Data(int counter)
{
this.counter = counter;
}

}
public class Demo {

static void changeData(Data a)
{
a.counter ++;
}
static void changeString(String a)
{
a="Change";
}
public static void main(String[] args) {
// TODO code application logic here
Data data = new Data(10);
changeData(data);

System.out.println(data.counter);

String str = "Original";
changeString(str);
System.out.println(str);
}

}

အေပၚက code သည္ ပထမ System.out.println အတြက္ data.counter အတြက္ဆုိရင္ 11 ထြက္လာပါလိ့မ့္မယ္။ ဒုတိယ System.out.println() အတြက္ဆုိရင္ေတာ့ Original ပဲထြက္လာပါလိမ့္မယ္။

method ၂ခုလံုးက Object ေတြကို pass လုပ္တာပါ။ changeData မွာက်ေတာ့ a.counter ++; ဆုိၿပီး parameter object a ရဲ. counter ကုိ ၁ တုိးတာပါ။ ဆုိခ်င္တာက Object reference a ရဲ. data ကုိယူသံုးတာပါ။

ဒုတိယ changeString မွာက်ေတာ့ ဘာကိုၿပင္လုိက္သလဲဆုိေတာ့ parameter a ရဲ. တန္ဖုိးကိုေၿပာင္းလုိက္တာပါ။ a = "Change" ဆုိၿပီး

အဲ့မွာ ပထမတခုကေတာ့ေၿပာင္းတယ္။ ဒုတိယတခုကေတာ့မေၿပာင္းဘူး ၂ ခုလံုးက Object ေတြအေနနဲ.သြားတာ။ Object ဆုိ pass by reference နဲ.သြားရမွာမဟုတ္ဘူးလား ဘာလုိ.ဒုတိယေကာင္က မေၿပာင္းတာလဲဆုိရင္ အေၿဖက Java မွာ pass by reference ဆုိတာမရိွလို.ပါပဲ။

အေပၚက code ရဲ.ၿပႆနာကိုနားလည္ဖုိ.က Java မွာ Object ေတြကို ဘယ္လိုသိမ္းလဲေပါ့။ ဥပမာ

String str = "Hello";
ဒီလိုဆုိရင္ str ထဲမွာ Hello ဆုိတဲ့ေကာင္ရိွေနတာမဟုတ္ဘူး Hello ဆုိတဲ့ string object ၾကီးကို str ဆုိတဲ့ reference ေလးကပဲညြွန္ထားတာဆုိတဲ့သေဘာ။ Reference သည္ တနည္းအားၿဖင့္ pointer ဒါမွမဟုတ္ memory address သေဘာယူဆလို.ရတယ္။တိုက္ရုိက္ေတာ့မတူဘူး JVM implmentation ေတြမွာဆုိ ဒါကို reference handle လုိ.ေခၚတယ္ ဆုိခ်င္တာက Object variable ေတြသည္ reference variable ထဲမွာ တုိက္ရုိက္သိမ္းတာမဟုတ္ဘူး ။ သူတုိ.ကို လွမ္းေထာက္လုိ.ရတဲ့ variable အေနနဲ.ပဲရိွေနတာ။

အဲ့ေတာ့ခုနက method ေတြကို parameter pass လုပ္တဲ့အခါ JVM အေပၚမွာ method တခု ကိုေခၚမယ္ဆုိရင္ Stack Frame တခုေဆာက္ရတယ္။ Stack frame ထဲမွာ local variable ေတြ အတြက္ ေနရာေတြ။ parameter variable ေတြအတြက္ေနရာေတြပါရတယ္။ ဒါဆုိ ခုနက method ေတြအတြက္ stack frame ေဆာက္တဲ့အခါ parameter အတြက္ stack frame ထဲမွာေနရာယူတဲ့အခါ reference ကိုသိမ္းဖုိ.ပဲေနရာလိုတယ္။ Reference size သည္ 32 bit VM မွာဆုိရင္ 32 ၿဖစ္ၿပီးေတာ့ 64 bit VM မွာဆုိရင္ 64 bit ၿဖစ္တယ္(JVM implementation အေပၚမူတည္ၿပီး size ကြာႏဳိင္တယ္) Object ေတြကေတာ့ Heap မွာေနရာသြားယူတယ္။ အဲ့ေတာ့ method call လုပ္မယ္ဆုိရင္ ခုနက main ထဲကေန argument (method call လုပ္ဖုိ. parameter ေနရာေတြမွာထဲ့ေပးလိုက္မဲ့တန္ဖုိးကို) copy ကူးလုိက္တယ္။ ဆုိခ်င္တာက changeData မွာေရာ changeString မွာပါ ဆုိင္ရာ reference ေတြသည္ copy ကူးသြားတယ္။

changeData မွာ reference က တဆင့္ညြန္တဲ့ variable ကုိေၿပာင္းတာၿဖစ္တဲ့အတြက္ မူရင္း Object မွာတန္ဖုိးေၿပာင္းတယ္။ changeString မွာက်ေတာ့ မူရင္း reference တန္ဖိုးကို ေၿပာင္းတာၿဖစ္တဲ့အတြက္ အဲ့ဒီ effect သည္ main မွာလာမၿဖစ္ဘူး ။ဘာလုိ.လဲဆုိေတာ့ seperate copy ၿဖစ္လုိ.ဒါေၾကာင့္ pass by value လုိ.ေၿပာတာ။

Reference ပံုသေဘာကို ၿမင္သာေအာင္ ပံုပါထဲ့ေပးလိုက္တယ္ ပံုကေတာ့ Credit ေပါ.

![Figure 1](https://github.com/LunaM00n/programming-collection/blob/master/Knowledges/1.jpg)

Java မွမဟုတ္ဘူး တခ်ိဳ. pass by value ပဲေပးတဲ့ language ေတြမွာလဲ သေဘာကေတာ့ဒီအတုိင္းပဲ။
