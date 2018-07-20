## Different Semantics in Programming Languages

Programming language ေတြ semantic ေတြ ဘယ္လိုကြာသလဲ

Java မွာ ေအာက္က code ကုိ run လုိ္က္ရင္ ဘာထြက္မယ္ထင္ပါသလဲ။

    int i=0;  
    i+= i++ ;  
    System.out.println(i);

1 ထြက္မယ္ဆုိရင္ေတာ့ မွားပါတယ္။ 0 ထြက္ပါတယ္။

ေကာင္းၿပီ ဘာလုိ. 1 မထြက္ပဲနဲ. 0 ထြက္ရတာလဲ။  
ခုနက code ကို C++ မွာ (System.out.print ေနရာမွာေတာ့ cout ေပါ့) ေၿပာင္း run ရင္ gcc compiler ေတြမွာ warning ေပးပါတယ္။ unsequenced modification and access to 'I' ဆုိၿပီးၿပပါတယ္။

ဒါေပမဲ့ အေၿဖကို run လိုက္ရင္ေတာ့ 1 ထြက္ပါတယ္။

ဒီ code ေလး ၂ေၾကာင္းကို ဘာလုိ. language ၂ခုမွာ ၂ မ်ိုးထြက္ေနတာလဲဆုိရင္ အေၿဖက semantic ေၾကာင့္ပါ။ Semantic ဆုိတာ program ေတြရဲ. meaning လို.ဆုိခ်င္တာပါ။ Program statement ေတြ expression ေတြသည္ ဘယ္လို အဓိပၺာယ္ရိွတယ္ဆုိတာကိုေၿပာတာပါ။

ကဲ ဒါဆုိ ခုနက Java က ဘာေၾကာင့္ 1 မထြက္ပဲ zero ထြက္တာလဲေပါ့။ C++ က်ေတာ့ 1 ထြက္တယ္ေပါ့။ အေၿဖကေတာ့ ရွုပ္ပါတယ္။ Java သည္ stack based VM ကိုသံုးလုိ.အဲ့လိုထြက္တာပါ။ က်န္တဲ့ stack based VM သံုးတဲ့ ဥပမာ JS, C# တုိ.လဲ အေၿဖ 0 ပဲထြက္မွာပါ။

C++ က်ေတာ့ register based ကိုသံုးတယ္ တုိက္ရုိက္ variable ေတြကို assembly code ကေန run တဲ့အတြက္ 1 ထြက္ရတာပါ။

ခုနက Java ကိစၥကိုရွင္းမယ္ဆုိရင္ အေပၚက code fragment ေလးကို javap နဲ. disassembly လုပ္ရင္ ဒီလို ဟာမ်ိဳးရပါလိ့မ္မယ္။

    public static void main(java.lang.String[]);  
    descriptor: ([Ljava/lang/String;)V  
    flags: ACC_PUBLIC, ACC_STATIC  
    Code:  
    stack=2, locals=2, args_size=1  
    0: iconst_0  
    1: istore_1  
    2: iload_1  
    3: iload_1  
    4: iinc 1, 1  
    7: iadd  
    8: istore_1  
    9: getstatic #2 // Field java/lang/System.out:Ljava/io/PrintStream;  
    12: iload_1  
    13: invokevirtual #3 // Method java/io/PrintStream.println:(I)V  
    16: return

Java bytecode လို.ေခၚတာေပါ့။

Java က အဲ့ bytecode ကိုဘယ္လုိ run သြားလဲဆုိတာသိဖုိ. JVM အေၾကာင္း stack အေပၚမူတည္ၿပီး expression ေတြ evaluate လုပ္တယ္ဆုိတဲ့အေၾကာင္း နားလည္ရပါလိ့မယ္။ အဲ့တာေတြကို JVM series မွာေရးထားပါတယ္။

Java မွာ method တခုကို ေခၚေတာ့မယ္ဆုိရင္ method ထဲမွာ သံုးတဲ့ parameter, ေတြ local variable ေတြရယ္ ဖုိ. local variable array နဲ. operand stack (expression ေတြကို evaluate လုပ္ဖုိ.) လိုတဲ့ memory ကုိေဆာက္ရပါတယ္။

ခုနက byte code မွာ stack 2 ဆုိတာ operand stack အတြက္ 2 word ေနရာယူမယ္။ locals 2 ဆုိတာလဲ 2 word ေနရာယူမယ္ (main ရဲ. parameter String array အတြက္ object reference ဖုိ. 1 word ရယ္ ေနာက္ၿပီး local variable I ဖုိ. 1 word ရယ္ စုစုေပါင္း 2 word ေပါ့)

stack=2, locals=2, args_size=1

ေကာင္းၿပီ  
Local variable array မွာ parameter ေတြကို အရင္သိမ္းတယ္။ ဒါေၾကာင့္ local variable I သည္ index 1 မွာ ေနရာရတယ္။

ေအာက္က code သည္ i=0 ကို လုပ္တာ။  
0: iconst_0  
1: istore_1

icons_0 ဆုိတာက constant 0 ကို operand stack ေပၚတင္မယ္။ istore_1 ဆုိတာက ခုနက operand stack ထိပ္ဆံုးမွာရိွတဲ့ 0 ကုိ local variable index 1 ေနရာမွာသိမ္းတယ္လုိ. အဓိပၺာယ္ရတယ္။

i+= i++ ; ကိုက်ေတာ့ ဒီ ေကာင္ေတြက လုပ္တာ။

2: iload_1  
3: iload_1  
4: iinc 1, 1  
7: iadd  
8: istore_1

iload_1 ဆုိေတာ့ local variable ထဲမွာရိွတဲ့ တန္ဖုိး (ခုနက 0 ထဲ့ထားတယ္) ကို operand stack ေပၚတင္တယ္။ အဲ့ေတာ့ operand stack က ဒီလိုရမယ္ stack ေအာက္ဆံုးသည္ ဘယ္ဘက္လုိ.မွတ္ပါ။

[ 0 ]  
ေနာက္တခါ 3:iload_1 ကို run ရင္ ဒီလိုရမယ္ operand stack က

[0 , 0]

ေနာက္ instruction 4

4: iinc 1, 1

သူက 0 ထြက္ေစတဲ့ အဓိက တရားခံပဲ။ သူက innc ဆုိတာ integer increment ကိုဆုိတာ။ ေရွ.က 1 သည္ local variable i ဖုိ. ေထာက္ထားတဲ့ index 1 , ေနာက္က ေကာင္သည္ တုိးမဲ့ေကာင္ 1

အဲ့ေတာ့ local variable ထဲမွာ i ေနရာမွာ 0 ကေန 1 ကုိေၿပာင္းသြားၿပီ။  
operand stack က ေတာ့ ဒီလို  
[0,0]

local variable array  
[ null, 1 ]

အဲ့လိုၿဖစ္ေနၿပီ

ဒါဆုိ line 7, ဒီမွာ java compiler က iကုိၿပန္ fetch မလုပ္ဘူး။ ဒါေၾကာင့္ stack ေပၚက ေကာင္ကိုပဲယူတယ္။ postfix ဆုိေတာ့ expression ၿပီးမွယူရတာကိုး ဒါေပသိ operand stack ေပၚမွာက်ေတာ့အဆင္မေၿပဘူး ၿဖစ္သြားတာ။

7: iadd  
8: istore_1

iadd ဆုိတာ integer 2 လံုးေပါင္းမယ္ေၿပာတာ. ဘယ္ကဟာကိုေပါင္းမွာလဲဆုိေတာ့ operand stack ေပၚက ဒါဆုိ operand stack ေပၚက 0,0 ကုိေပါင္းေတာ့ 0 ရ အဲ့ေကာင္ကို operand stack ေပၚၿပန္တင္ 0

ဒါဆုိ line 7 ၿပီးသြား၇င္ operand stack မွာ  
[0] ၿဖစ္ေနမယ္။

ဒါဆုိ ခုနက line 8 ကုိ run လိုက္ေရာ 0 ကို local variable i ေနရာမွာသြားသိမ္းေရာ။ အဲ့ေနရာေၾကာင့္ stack based machine ေၾကာင့္သာ 0 ၿဖစ္သြားတာ။ ဘာလို.လဲဆုိေတာ့ i ရဲ. မူလတန္ဖိုး 1 ကုိ store မလုပ္ ခင္မွာ မေခၚလိုက္မိလုိ.ပဲ။

C++ မွာက်ေတာ့ assignment မလုပ္ခင္မွာ i တန္ဖုိး 1 ကိုၿပန္ေခၚတယ္။ fetch လုပ္တယ္ေပါ့။

အဓိကအခ်က္ ဒီေနရာမွာ semantic ကြာတာသည္ Java က expression evaluation မွာ operand stack ကိုသံုးတယ္ variable တန္ဖိုးေတြကို stack ေပၚcopy လုပ္လို႔ C++ က်ေတာ့ variable ေတြကို register ေတြကတဆင့္တိုက္႐ိုက္သံုးၿပီး evaluate လုပ္လို႔

ဒီေလာက္ဆုိ ++ အေၾကာင္း ေရးေတးေတးေတာ့သေဘာေပါက္ေရာေပါ့ ![](https://static.xx.fbcdn.net/images/emoji.php/v9/eb4/1/16/FACE_WITH_COLON_THREE.png)

ဟို language လဲ ဒါပဲ ဒီ language လဲဒါပဲဆုိရင္ ဒါေလး ၿပလိုက္ပါလို. ![](https://static.xx.fbcdn.net/images/emoji.php/v9/f9f/1/16/1f61b.png)
