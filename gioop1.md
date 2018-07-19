## Gentle Introduction to Object Oriented Programming - Part 1

ခုေလာေလာဆယ္ Industry မွာ အသံုးအမ်ားဆံုး programming language paradigm အရဆိုရင္ေတာ့ Object Oriented Programming က popular အၿဖစ္ဆံုးလို.ေၿပာရမွာပါ။ 
အသံုးမ်ားတဲ့ OO Language ေတြကေတာ့ *Java, C#, JavaScript, PHP, Ruby , Python* တို.ပါပဲ၊ 
**Language** တခုကိုေလ့လာတဲ့အခါမွာ element ၃ ခုကိုေလ့လာရပါတယ္။ Syntax, Semantic နဲ. Pragmatic တို.ၿဖစ္ပါတယ္။ 
**Syntax** ကေတာ့ရွင္းပါတယ္ language basic component ေတြကို ဘယ္လုိေရးရတာလဲဆုိတဲ့ Grammar ပါ။ ဥပမာ for loop ပတ္ရင္ဘယ္လိုေရးရသလဲေပါ့။ 
**Semantic** ကေတာ့ for loop ေရးထားရင္ for loop ကဘယ္လုိအလုပ္လုပ္မလဲဆုိတဲ့ တိက်တဲ့အဓိပၸာယ္ကို ဆုိခ်င္တာပါ။ ဥပမာ for initialization ရိွရင္ run မယ္။ေနာက္ for conditional ရိွရင္စစ္မယ္ result က true ဆုိရင္ for body ကို execute မယ္။ ၿပီးရင္ for increment ရိွခဲ့ရင္ သူ.ကို run မယ္ ေနာက္ loop အစကိုၿပန္တက္မယ္ condition ၿပန္စစ္မယ္ ေပါ့။ ဒါေတြကို semantic လို.ေခၚရမွာပါ။ 

*Programming သင္တယ္လို.ေၿပာလိုက္ရင္ syntax ကုိပဲသင္ၾကတာကို ေတြ.ရပါတယ္။* 

language 2 ခုက syntax အရ ဆင္နုိင္ပါတယ္ ဒါေပမဲ့ semantic အရ မတူႏုိင္ပါဘူး ဥပမာ for loop ဆိုပါစုိ. C,C++,Java,C#,JavaScript တုိ.မွာ syntax အရသိပ္မကြာပါဘူး ဒါေပမဲ့ semantic အရ မတူႏုိင္ပါဘူး။ 
ဥပမာ C/C++/JavaScript မွာ conditinal part ဟာ boolean မဟုတ္တဲ့ integer တခုခု (*JS မွာဆုိ Object type ပါၿဖစ္နုိင္ပါတယ္*) ၿဖစ္ခြင့္ရိွေပမဲ့ Java,C# မွာဆုိရင္ boolean type ကိုၿဖစ္ရမွာပါ။
ေနာက္တခုက for initialization မွာ variable ေၾကၿငာ ခဲ့ရင္ C,C++,Java,C# မွာဆုိရင္ for loop အတြင္းမွာပဲ variable scope ကရိွေပမဲ့ JavaScript မွာဆုိ the whole function တခုလံုးလို.ေၿပာရမွာပါ။ ဒါဟာ semantic အရ မတူေၾကာင္းကုိေၿပာတာပါ။

ေနာက္တခုက **Pragmatic** ပါ။ သူကေတာ့ language တခုရဲ. construct ေတြကို လက္ေတြ.က်က်ဘယ္လိုသံုးရမလဲဆုိတာပါ။ Programming language တခုကေပးထားတဲ့ feature ေတြ language construct ေတြကို သင့္ေတာ္မွန္ကန္စြာ အသံုးခ်ႏုိင္မွု.ပါ။ ဘာကိုဆုိခ်င္သလဲဆုိေတာ့ OO paradigm ကို support ေပးတဲ့ language မွာ OO program ေတြကို ဘယ္လိုေရးရသလဲ ။ ဥပမာ ဘယ္အခ်ိန္မွာ inheritance ကုိသံုးလဲ ရုိးရုိး class ကုိသံုးရမွာလား abstract class ကုိသံုးရမွာလား abstract class နဲ. interface usage ဘယ္လိုကြာလဲ ဘယ္ေနရာဘယ္သူ.ကိုသံုးရမွာ correct usage က ဘာေတြလဲ ဒါေတြကို ဆုိခ်င္တာပါ။ Pragmatic ကုိအဆင့္ထပ္ၿမွင့္ရင္ေတာ့ design pattern ေတြ ,principle ေတြ ပါ ပါလာမွာပါ။ Programmer တေယာက္အေနနဲ. Language construct ေတြ paradigm နဲ.ပတ္သတ္တဲ့ concept ေတြကိုသိဖုိ.လုိပါတယ္။ Java နဲ.ေရးေနေပမဲ့ C မွာေရးသလို function ေတြနဲ.ပတ္လည္ေရးေနတယ္ဆုိရင္ မဟုတ္ေတာ့ပါဘူး။

### Evolution to OOP

Modern high level Programming language ေတြမေပၚခင္က machine language သို.မဟုတ္ assembly language ကိုသံုးရပါတယ္။ Assembly ကုိသံုးရတာဟာ machine language ကုိ symbolic code အစားထုိးသံုးရတာနဲ.ဘာမွမကြာပါဘူး။ သိပ္မဟန္ပါဘူး ။ဒါေၾကာင့္ high level language ေတြထုတ္ပါတယ္။ အေစာပုိင္းက data structure နဲ. algorithm ေတြေရးလုိ.အဆင္ေၿပေအာင္ ထုတ္ထားတဲ့ Procedural Language(Fortan, Algo, C) ေတြေပၚလာပါတယ္။ Procedural language ေတြရဲ.အဓိက concept ကေတာ့ fuction ေတြခြဲေရးမယ္ ။ function ေတြကို reusable ၿဖစ္ေအာင္လုပ္မယ္။ ဒီလိုနည္းနဲ.သြားပါတယ္။ ေနာက္က်ေတာ့ data abstraction ကိုထဲ့လာပါတယ္။

### Data Abstraction

Data Abstraction ဆုိတာ custom data type ေတြ create လုပ္ခြင့္ေပးထားတာကိုေၿပာတာပါ။ ဥပမာ Stack, LinkedList ဆုိတာမ်ိဳးကို data type တခုအေနနဲ.ကုိယ္ပုိင္ ဖန္တီးလို.ရမယ္။ ၿပန္သံုးလုိ.ရမယ္ ဒါကို data abstraction လို.ေၿပာလုိ.ရပါတယ္။ ဥပမာ C မွာ ဆုိ struct, enum, class ဆိုတာ data abstraction ေတြေပးထားတာပါ။ Primitive type ေတြကေန custom data type ဖန္တီးလို.ရမယ္ အဲ့ data type ကို maniuplate လုပ္ဖုိ. function ေတြ create လုပ္လုိ.ရမယ္ဆုိရင္ အဲ့ဒီ language ကို data abstraction ေပးတယ္လို.ေၿပာရမွာပါ။

### Beginning of OOP

Data abstraction ေၾကာင့္ custom data type ေတြ ေတာ့ဖန္တီးလို.ရပါၿပီ။ ဒါေပမဲ့ ၿပႆ နာ တခုက သူ.ကိုၿပင္မယ္ဆုိရင္ ဆုိပါစုိ. existing ADT(Abstract Data Type) တခုကိုၿပင္မယ္ဆုိရင္ သူ. source code ကုိၿပင္ရမွာပါ။ ဒါကုိ destructive modification လုိ.ေခၚပါတယ္။ အဲ့ဒါက အႏၱရာယ္မ်ားပါတယ္ ဘာလုိ.လဲဆုိေတာ့ project တခုမွာ ADT တခုကုိ reference လုပ္ၿပီးသံုးထားတဲ့ code ေတြ အမ်ားၾကီးရိွႏုိင္လို.ပါ။ ADT ရဲ. source code ကုိမထိပဲၿပင္ႏုိင္တဲ့ နည္းကေတာ့ OOP သံုးၿပီး inheritance နဲ. functionality အသစ္ကို ထပ္ထဲ့တာ existing method ကို modify လုပ္တာပါပဲ။ ဒါဆုိ ရိွၿပီးသား code ကို မထိပဲနဲ. ၿပင္လုိ.ရပါၿပီ။ Software ဆိုတာ ေရးၿပီးတာနဲ.ၿပီးတာမဟုတ္ပဲ အၿမဲ ေၿပာင္းလဲေနႏုိင္ပါတယ္ OOP ရဲ. feature ေတြက ဒါေတြကို handle လုပ္ႏုိင္ပါလိမ့္မယ္။

### Data Abstraction versus OOP

Data abstraction က custom data type ေတြ တည္ေဆာက္လို.ရမယ္။ OOP ၿဖစ္ဖုိ.ကေတာ့ ေအာက္ပါ သံုးခ်က္ကုိမၿဖစ္မေနေပးရပါတယ္။ အဲ့ဒါေတြကေတာ့ Encapsulation Inheritance Polymorphism

တို.ပါပဲ။ Object ေတာ့ေပးေဆာက္တယ္ feature သံုးခုလံုးမပါဘူဆုိရင္ Object based language လို.ပဲေခၚမွာပါ ဥပမာ Visual Basic( VB.NET ကေတာ့ OOP Feature သံုးခုလံုးေပးထားပါတယ္). OO language ရဲ.အားသာခ်က္ထဲက တခုက ေတာ့ conceptual modelling ပါပဲ၊ အရင္က software development ကို function ေတြ algorithm ေတြနဲ.စဥ္းစားမဲ့အစား real world မွာရိွတဲ့အတုိင္း object ေတြအေနနဲ. စဥ္းစားရတဲ့ ပုိလြယ္ကူပါတယ္။ real world မွာရိွတဲ့ အတုိင္း classification (by mean of class), taxonomy (by mean of inheritance), specialization (by mean of polymorphism) အတုိင္း model လုပ္လို.ရသြားပါတယ္။

### Pure and Impure OO Language

Programming language တခုဟာ Object ကလြဲၿပီး တၿခား construct ေတြေပးမထားဘူးဆုိရင္ သု.ကုိ pure Object Oriented Language လို.သံုးပါတယ္။ ဥပမာ Smalltalk မွာဆုိ loop ဆုိတာမ်္ိဳး မရိွပဲ loop ဆိုတာကို method တစ္ခုအေနနဲ.ယူဆပါတယ္။ integer လိုေကာင္မ်ိဳးေတြကအစ object ေတြပါ ဒါေၾကာင့္ pure OO language လို.သံုးပါတယ္။ ဘာေကာင္းလဲဆုိေတာ့ program တစ္ခုလံုးကုိ OO နည္းနဲ.ပဲစဥ္းစားရေအာင္ လုပ္ထားတာပါ။ C++, Java,C#,JS တုိ.ကေတာ့ impure object oriented language လို.ေၿပာရမွာပါ။ သူတုိ.မွာ primitive data type ေတြပါၿပီး control structure (for/switch etc) ေတြပါလုိ.ပါ။

### Encapsulation

Procedural language ေတြမွာ data ကိုဘံုထားၿပီး function ေတြကေန၀ုိင္းသံုးၾကပါတယ္။ Project size ၾကီးလာတာနဲ.အမွ် အဲ့ဒီ ဘံုသံုးထားတဲ့ variable(global variable) ေတြကို ဘယ္ module, ဘယ္ function ကသံုးထားတယ္ဆုိတာ လိုက္ၾကည့္ဖု.ိေတာ္ေတာ္ခက္သြားပါၿပီ။ PHP မွာဆုိ global variable သံုးၿပီး page အမ်ားၾကီး ၀ုိင္းသံုးတာမ်ိဳးပါ။ ေနာက္ၿပီး ကိစၥရိွလုိ. အဲ့ဒီ global variable ကုိၿပင္မယ္ဆုိရင္ သူ.ကို သံုးထားတဲ့ module ေတြ function ေတြကို ပါလိုက္ၿပင္ရမွာပါ။ တခုခုကုိၿပင္ရင္ တၿခား အပိုင္းေတြပါ ထိခုိက္ကုန္ပါတယ္။ ဒါေၾကာင့္ OO language မွာ အဲ့တာကုိမၿဖစ္ေအာင္ ကာၾကပါတယ္။ Program ေတြကုိ modular ၿဖစ္ေအာင္ေရးဖုိ.ၾကံဆၾကပါတယ္။ Modular ၿဖစ္တယ္ဆုိတာ program module, function, contruct တခုဟာ သူ.ဟာသူနဲ.ရပ္တည္ႏိုင္ရပါမယ္။ သူမ်ား function ေတြကုိ အမ်ားၾကီးသံုးေနရတာ dependency မ်ားေနတာ မၿဖစ္ရပါဘူး။ Modular ၿဖစ္မွ dependency နည္းမွပဲ ၿပင္ရတာ လြယ္ကူမွာၿဖစ္ပါတယ္။ ဒါေၾကာင့္ global variable အစား ကုိ. data ကုိပဲသံုးမယ္ သူမ်ားက လာသံုးမရေအာင္ access ကုိ restrict လုပ္ထားမယ္ သူ. data ကို သူ. method ေတြကပဲသံုးမယ္ တၿခားေသာ module ေတြက ဒီ module ကုိ သံုးခ်င္ရင္ module ကေပးထားတဲ့ public interface(publicly accessible method) ေတြ ကေန သံုး။ ဒါဆုိရင္ တၿခား module ေတြဟာ သူမ်ားရဲ. data ကိုသြားထိလုိ.မရတဲ့အတြက္ သီးသန္.ဆန္သြားတဲ့အတြက္ modularity ပုိေကာင္းပါတယ္။ module တခုကုိၿပင္မယ္ဆုိရင္ public interface(public interface ကပဲသူမ်ား module နဲ. dependence ၿဖစ္ပါတယ္) ကိုမၿပင္မခ်င္း လြတ္လြတ္လပ္လပ္ၿပင္ႏိုင္မယ္။ ဒါကို encapsulation လို.သံုးပါတယ္။ Encapsulation ရဲ.အႏွစ္သာရက ကို. data ကိုသူမ်ားက accidentally destroy မၿဖစ္ေအာင္ dependency မရိွေအာင္ ထားရတာပါ။ Encapsulation ကို data hidiing နဲ.တြဲသံုးပါတယ္။ Encapsulation နဲ. data hiding ဟာ တူသလုိလုိနဲ. ကြဲပါတယ္ data hiding က ကုိ.data ကုိၿပင္ပက လာသံုးလုိ.မရေအာင္ကာထားတာမ်ိဳးပါ။ Encapsulation ကေတာ့ data ကို ကုိ. function ေတြနဲ. modularity ရေအာင္ ခ်ိတ္သံုးတာကို ဆုိခ်င္တာပါ။ Java, C#, C++ မွာဆုိ private accessifier ေတြသံုးၿပီး encapsulation ရေအာင္လုပ္ၾကပါတယ္။ Member variable ကုိ Private ထားၿပီး getter ,setter function ေတြနဲ.သံုးၾကပါတယ္။ အဲ့လိုသံုးတုိင္း encapsulation မရႏဳုိင္ပါဘူး ။ ေအာက္က Java Program ကုိၾကည့္ပါ။

    class WrongEncapsulation 
    { 
    private CreditCard card; 
    public void setCard(CreditCard c){...} 
    public CreditCard getCard() 
    { 
    return card; 
    } 
    }

 ဒီ Program မွာ card က private ပါ reference type ပါ။ သူ.ကုိ တုိက္ရုိက္ယူသံုးလုိ.မရေပမဲ့ getCard ကေန ယူသံုးလုိ.ရ႔ပါတယ္။ဒါဆို တနည္းအားမ်ား card ကုိ တုိက္ရုိက္ယူသံုးႏိုင္တာနဲ.အတူတူပါပဲ။ Java က reference model ကိုသံုးတဲ့အတြက္ အၿပင္ကေန card ကို ၿပင္လုိ.ရမွာပါ။ဒါဆုိ encapsulated ၿဖစ္တယ္လုိ.မေၿပာႏုိင္ေတာ့ပါဘူး။ JavaScript လို language မ်ိဳးက်ေတာ့ access modifier မပါပါဘူး ဒါေပမဲ့ full encapsulation ကိုလုပ္လုိ.ရပါတယ္။ Closure သံုးၿပီး encapsulate လုပ္ႏုိင္ပါတယ္။

    <script> 
    function getObject() { 
    var data; 
    function dataGetter() 
    { return data; } 
    function dataSetter(d) 
    { data = d; } 
    return { setData : dataSetter, getData : dataGetter }; } 
    var obj = getObject(); obj.setData(100); 
    console.log(obj.getData()); 
    </script>

အေပၚမွာၿပထားတဲ့ JavaScript code မွာ encapsulation ကုိၿပထားပါတယ္။ getObject function ထဲမွာရိွတဲ့ data ဟာ encapsulated လုပ္ခံထားရတာပါ။ သူ.ကုိအၿပင္ကေန တုိက္ရုိက္ယူသံုးလို.မရပါဘူး။ ဘာလုိ.လဲဆုိေတာ့ local varaible မုိ.လို.ပါ။ getObject function ေအာက္ဆံုးမွာ object တခု return ၿပန္ထားပါတယ္ အဲ့မွာ setData, getData ကို getObject function ထဲက dataSetter,dataGetter ကုိေပးထားပါတယ္။ dataSetter,နဲ. dataGetter ဟာ inner function ေတြၿဖစ္တဲ့အတြက္ data ကုိ enclosing scope က data ကုိယူသံုးလုိ.ရပါတယ္ ။ သူတုိ.ကုိေတာ့အၿပင္ကေန တုိက္ရုိက္သံုးလို.မရပဲ setData နဲ. getData ကတဆင့္သံုးရမွာပါ။ JS မွာဒီနည္းနဲ. Encapsulation ထိန္းလို.ရပါတယ္။ Encapsulation ဆိုတာ class level ထိန္းမွမဟုတ္ပါဘူး package , module ေတြဟာလဲ ၿပင္ပ ကေကာင္ေတြတုိက္ရုိက္သံုးလို.မရေအာင္ ထိန္းေပးထားတဲ့ encapsulation construct ေတြပါပဲ။ Encapsulation နဲ. ပတ္သတ္တဲ့ OO Principle တခုရိွပါတယ္ အဲ့ဒါကေတာ့ Program to interface, not to implementation ပါ။ Program ေရးတဲ့အခါမွာ module ေတြ class ေတြဟာ သူမ်ားရဲ. implementation detail ကိုမသိသင့္ မထိသင့္သလိုု. ကုိ.ဟာကုိလဲ expose မလုပ္သင့္ပါဘူး။ အၿပင္ကသံုးမဲ့ ကုိနဲ.တကယ္ interact ေပးလုပ္မဲ့ေကာင္ေတြကုိပဲ public interface အေနနဲ.ထားေပးရမယ္ဆုိလုိတာပါ။ ဒါမွ maintenance ေကာင္းမွာပါ။Encapsulation နဲ.ပတ္သတ္တဲ့ တၿခား OO principle တခုကေတာ့ Open Close Principle ပါပဲ။ A module should be open for extension but closed for modification. Module ေတြ classes ေတြဟာ သူတုိ.ကုိ accidentally modified မလုပ္ႏိုင္ေအာင္ထားသင့္ၿပီးေတာ့ extend လုပ္ႏိုင္ေအာင္ေတာ့ ထားေပးရမယ္ဆိုတာပါ။ Encapsulation ရဲ. central theme ကိုက close for modification ပါပဲ။
