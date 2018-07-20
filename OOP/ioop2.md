## Introduction to Object Oriented Principles - Part 2

လုိက္နာရမဲ့ Principle ေတြ မေၿပာခင္မွာ ေရွာင္သင္တဲ့ principle ေတြ အရင္ေၿပာပါမယ္ ဒါကေတာ့ STUPID ပါ။ STUPID အရွည္ေကာက္ကေတာ့ ေအာက္ပါအတုိင္းပါ

Singleton Tight Coupling Untestability Premature Optimization Indescriptive Naming Duplication

**Singleton**

Singleton design pattern ဆုိတာ GoF(Gang of Four) major design pattern ၂၃ မ်ိဳးထဲမွာ တစ္ခုအပါအ၀င္ပါပဲ။ သူ.ကုိ ဘာအတြက္သံုးလဲဆုိရင္ေတာ့ class တခုကုိ single instance ပဲလိုခ်င္ရင္ သံုးပါတယ္။ ဆုိခ်င္တာက class တခုအတြက္ object တစ္ခုပဲေဆာက္ခ်င္တာေပါ့။ ဘယ္လိုေနရာမ်ိဳးမွာ အသံုး၀င္လဲဆုိေတာ့ globally available ၿဖစ္တဲ့ တစ္ခုထက္ပုိေဆာက္ဖုိ.မလိုတဲ့ object မ်ိဳးလိုရင္ သူ.ကုိသံုးလို.ရပါတယ္။ ဥပမာ သာမာန္ small application ေတြမွာ DAO connector အတြက္ singleton ကုိသံုးလို.ရပါတယ္။ Application တခုလံုးမွာ single object ပဲရိွေနေစခ်င္ရင္ singleton ကုိသံုးပါတယ္။ Java မွာဆုိရင္ေတာ့ java.lang.Runtime class နဲ. java.awt.Desktop တုိ.ဟာ singleton class ေတြပါ။ Runtime class ဆုိတာ ခုလက္ရိွ run ေနတဲ့ OS နဲ.ပတ္သတ္ၿပီး process ေတြ execute လုပ္ခ်င္ရင္သံုးလုိ.ရတဲ့ method ေတြ ေတာ္ေတာ္မ်ားမ်ားပါ ပါတယ္။ Runtime object ကုိတစ္ခုထက္ပိုေဆာက္ဖုိ.မလိုပါဘူး ဘာလုိ.လဲဆုိေတာ့ OS runtime က တစ္ခုထဲရိွလို.ပါ။ အဲ့လိုေနရာေတြမွာ Singleton ကုိသံုးေပမဲ့လဲ အလြန္အကြ်ံသံုးမယ္ဆုိရင္ singleton ဟာ bad pattern ၿဖစ္လာပါတယ္။ Singleton pattern ရဲ.မေကာင္းတဲ့အခ်က္ေတြက ေအာက္ပါအတုိင္းၿဖစ္ပါတယ္။

Global vairable ပံုစံၿဖင့္ အသံုးၿပဳတဲ့အတြက္ singleton classes ဟာ application တခုလံုးမွာ ေနရာအႏွံ.ပါေနႏုိင္ပါတယ္။ ဒါက ဘာကိုၿဖစ္ေစလဲဆုိေတာ့ tight coupling between classes ကိုၿဖစ္ေစႏုိင္ပါတယ္။ Singleton object ေတြဟာ application အစကေန အဆံုးထိ lifetime ရိွႏုိင္ပါတယ္။ ဒါက performance ကုိက်ေစႏုိင္ပါတယ္။ ေနာက္တခုက singleton object ေတြဟာ သူတုိ.ရဲ. state (variable )ေတြကို persistence state (အေသထားထားတဲ့အတြက္) unit testing code ေတြေရးတဲ့အခါမွာ singleton object ေတြဟာ ဒုကၡေပးႏုိင္ပါတယ္။

ဒါဆုိ singleton မသံုးပဲဘယ္လိုလုပ္မလဲ ေပါ့။ ရွင္းပါတယ္ new နဲ. object တစ္ခုအၿပင္ကေနေဆာက္ၿပီးေတာ့ လုိတဲ့ module ဆီကုိ dependency injection သံုးၿပီး ပို.လိုက္ပါ။ Singleton ကုိအလြန္အကြ်ံမဟုတ္ပဲ ေတာ္သင့္ရံုပဲသံုးမယ္ဆုိလဲ ၿပ ႆ နာကို အထုိက္အေလ်ာက္ေၿပလည္ႏုိင္ပါလိမ့္မယ္။ Principle ဆုိတာ အတိအက်လုိက္နာရမယ္ဆုိတာ မဟုတ္ပါဘူး။ Rule မဟုတ္ပါဘူး ။

**Tight Coupling**

အရင္အပုိင္းမွာ Coupling နဲ. tight coupling အေၾကာင္းကိုရွင္းထားၿပီးပါၿပီ။ Coupling ကိုၿပန္ေၿပာရမယ္ဆုိရင္ program class တခု module တခုဟာ သူ.ရဲ. responsibility (behaviour or functionality, set of method) အတြက္ တၿခား module သုိ.မဟုတ္ class ေတြကို တုိက္ရုိက္ ယူသံုးရမယ္ဆုိရင္ ဒါဟာ coupled ၿဖစ္တာပါပဲ။ Tight coupled ၿဖစ္ေနတာကို ဥပမာ ၿပရရင္ ကြ်န္ေတာ္တုိ. window မွာ run လုိ.ရတဲ့ application ကုိသံုးတယ္ဆုိပါစို. ဒါဆုိ ကြ်န္ေတာ္တုိ.ရဲ. application ဟာ window os အေပၚမွာ coupled ၿဖစ္သြားပါၿပီ။ Coupled ၿဖစ္သြားေတာ့ဘာၿဖစ္လဲေပါ့ တကယ္လုိ.ကြ်န္ေတာ္တုိ.က OS ကုိေၿပာင္းမယ္ upgrade လုပ္မယ္ဆုိရင္ အဆင္မသင့္ရင္ ကြ်န္ေတာ္တုိ. application ဟာ သံုးလို.မရတာ ဒါမွမဟုတ္ အဆင္မေၿပတာမ်ိဳးၿဖစ္မွာပါ။ ဘာလုိ.လဲဆုိေတာ့ ကြ်န္ေတာ္တုိ. application ဟာ window အေပၚကုိ coupled ၿဖစ္ထားလုိ.ပါ။ ဒီသေဘာပါပဲ class တခု သုိ.မဟုတ္ module တခုဟာ တၿခားတခုကုိ မီွခုိေနရတယ္ coupled ၿဖစ္ေနရတယ္ဆုိရင္ သူမီွခုိရတဲ့ class or module ေၿပာင္းတုိင္းမွာသူက လိုက္ေၿပာင္းရမဲ့ဒုကၡ ရိွပါတယ္။ ဒါက maintenance ကို မေကာင္းေစပါဘူး။ ေနာက္တခုက testing လုပ္ေတာ့မယ္ဆုိရင္ အဆင္မေၿပပါဘူး။ ဒီေနရာမွာ testing ဆုိတာ unit testing ကိုေၿပာတာပါ။ unit testing ဆုိတာ program တခုရဲ. smallest functionality ကုိ code ေရးၿပီး test လုပ္တာကိုေၿပာတာပါ။ ဥပမာ class A သည္ class B ကုိ မွီခုိတယ္ coupled ၿဖစ္တယ္ေပါ့ ဒါဆုိရင္ class A ကုိ test code ေရးဖုိ.အတြက္ class B ကို ကြ်န္ေတ္ာတုိ.လုိပါၿပီ ။ အဲ့ဒါေၾကာင့္ testing မွာ အဆင္မေၿပဘူးေၿပာတာပါ။ ဒါဆို coupling မရိွလို.ရလားဆုိေတာ့မရပါဘူး။ loosely coupled ေတာ့ၿဖစ္ေအာင္လုပ္လုိ.ရပါတယ္။ ဒါဆုိ tight coupling ဆုိတာ ဘာကိုလဲဆုိတာထပ္ရွင္းရပါမယ္။ class တခုဟာ တၿခား class တခုကုိ highly dependence ၿဖစ္ေနတယ္ဆုိရင္ ဒါက tight coupling ပါ။ class တခုဟာ တၿခား class တခုကုိ ေအာက္ပါ အေၾကာင္းေတြေၾကာင့္ coupled ၿဖစ္ႏုိင္ပါတယ္။

တၿခား class ၏ Data ,instance variable မ်ားကို တုိက္ရုိက္ယူသံုးၿခင္း ၊ dot ေခါက္ၿပီး တၿခား class ကေကာင္ေတြကို တုိက္ရုိက္ယူသံုးတာပါ။ တၿခား class ၏ public interface (public method or behaviour) ကိုတုိက္ရုိက္ယူသံုးၿခင္း တၿခား class ၏ object အား new သံုးၿခင္းသုိ.မဟုတ္ အၿခားနည္းၿဖင့္ object ေဆာက္ၿခင္း

အထက္ပါ အခ်က္ေတြေၾကာင့္ coupling ၿဖစ္ႏုိင္ပါတယ္။ ပထမဆံုး အခ်က္ဆုိရင္ tightly coupled ၿဖစ္ေနၿပီလုိ.ေၿပာလို.ရပါတယ္။ encapsulation ကုိခ်ိဳးေဖာက္ရာလဲက်ပါတယ္။ Tight coupling က maintenance ကိုေရာ testing ကုိေရာ ထိခုိက္ႏုိင္ပါတယ္။ class Message { String content; //other behaviour of Message public void send() { EmailSender sender = new EmailSender(); sender.send(this); } } class EmailSender { public void send(Message msg) { //Mail sending code } }

အေပၚက class 2 ခုကို ၾကည့္ပါ။ အဲ့ ၂ခုမွာ class Message သည္ EmailSender class ကုိ tightly coupled ၿဖစ္ေနပါတယ္။ ဆုိခ်င္တာက Message class ရဲ. send မွာ EmailSender ကုိယူသံုးထားပါတယ္။ Object ေဆာက္တဲ့အၿပင္ send ဆုိတဲ့ method ကိုပါယူသံုးထားတာပါ။ အဲ့ေတာ့ EmailSender သာ တခုခုေၿပာင္းရင္ ဥပမာ EmailSender ရဲ. constructor ကို no argument မဟုတ္ပဲ တၿခား constructor ေၿပာင္းခဲ့မယ္ဆုိရင္ (ဒါက ဥပမာပါ EmailSender ဟာ တၿခားနည္းနဲ.လဲေၿပာင္းႏုိင္ပါတယ္) Message က ယူသံုးတဲ့ EmailSender ရဲ. constructor နဲ. send method ေတြ သာ တနည္းနည္းနဲ.ေၿပာင္းခဲ့မယ္ဆုိရင္ ကြ်န္ေတာ္တုိ.ရဲ. Message class ကုိ Effect ၿဖစ္မွာပါ ဒါက Tight coupling ေၾကာင့္ၿဖစ္တဲ့ၿပ ႆ နာပါ။ ေနာက္တခုက ကြ်န္ေတ္ာတုိ.ရဲ. Message class ကို unit testing code ေရးခဲ့မယ္ send method အတြက္ဆုိပါေတာ့ အဲ့ေကာင္အတြက္ unit testing code ေရးေတာ့မယ္ဆိုရင္ အဆင္မေၿပပါဘူး။ Unit testing ရဲ.သေဘာတရားက တခုခုကုိစမ္းတဲ့အခါမွာ သူတုိ.ခ်ည္း ပဲစမ္းလုိ.ရရင္အဆင္ေၿပပါတယ္ ဥပမာ class တခုကုိစမ္းဖုိ.ေနာက္ class တခုကုိ လုိမယ္ဆုိရင္ error တက္တဲ့အခါ ဘယ္ class ကတက္တာလဲဆုိတာ ေၿပာရခက္ပါတယ္ဒါေၾကာင့္ပါ။ ဒါေၾကာင့္ coupling ကိုေလ်ာ့ခ်င္ရင္ EmailSender object ကုိ Message send ဆီကုိပုိ.လိုက္ရင္ coupling နည္းသြားမွာပါ။ unit testing code ေရးမယ္ဆုိရင္လဲ ကြ်န္ေတ္ာတုိ.က EmailSender mock object တခုပို.လိုက္ယံုပါပဲ။ ေအာက္က code ဟာ ပုိၿပီးေတာ့ coupling နည္းသြားပါတယ္။

    class Message 
    { String content; //other behaviour of Message
    
    public void send(EmailSender sender) 
    { sender.send(this); } 
    }
    
    class EmailSender 
    { public void send(Message msg) 
    {
    
    //Mail sending code } 
    }

အေပၚကေပးထားတဲ့ example မွာ EmailSender ကုိ Message ရဲ. send ထဲမွာ new နဲ. object မေဆာက္ေတာ့ပဲ parameter အေနနဲ.အၿပင္ကေနေပးလိုက္တဲ့အတြက္ Dependency Injection သံုးၿပီး ထဲ့လို.ရသြားပါၿပီ ။ဒါဆုိ coupling နည္းသြားပါၿပီ။ ဒါေပမဲ့ Message သည္ concrete class ၿဖစ္တဲ့ EmailSender အေပၚမွာ coupled ၿဖစ္ေနတံုးပါ။ ဘာၿပ ႆ နာရိွလဲဆုိေတာ့ ကြ်န္ေတာ္တုိ.က ေနာက္ထပ္ EmailSender(ဆုိပါစုိ.ဗ်ာ code က requirement ေၾကာင့္ gmail နဲ.မပုိ.ေတာ့ပဲ yahoo mail server သံုးမယ္ ဒါမွမဟုတ္ email sending API တခုခုေၿပာင္းသြားတယ္ဆုိရင္ ကြ်န္ေတာ္တုိ. code က maintenance အတြက္ အဆင္မေၿပပါဘူး)ဒါေၾကာင့္ concerte class ကုိ coupled လုပ္မဲ့အစား EmailSender interface ထုတ္ၿပီးအၿပင္ကေန Dependency Injection နဲ.ထဲ့ေပးလုိက္ရင္ပိုအဆင္ေၿပမွာပါ။ ဒါဆုိ Message သည္ concrete class EmailSender အေပၚမွာ မမွီခုိေတာ့ပဲနဲ. interface EmailSender မွာပဲ copuled ၿဖစ္တဲ့အတြက္ different implementation ေပးႏုိင္မွာပါ အဲ့ေတာ့ code ကပိုၿပီး maintainable ၿဖစ္မွာပါ။ ေနာက္ဆံုးပံုစံက ဒီလိုၿဖစ္မွာပါ။

    class Message 
    { String content; //other behaviour of Message
    
    public void send(EmailSender sender) 
    { sender.send(this); } 
    }

interface EmailSender { public void send(Message msg); } class EmailSenderImplOne implements EmailSender { public void send(Message msg) { //Implementation Code } } အေပၚမွာေရးထားတဲ့ code အရ coupling ကုိေလ်ာ့လိုက္တဲ့အတြက္ EmailSender ကုိ EmailSendImplOne အၿပင္တၿခား ေနာက္မွာလိုေသးရင္ ထပ္ထဲ့လို.လြယ္ပါလိမ့္မယ္ ဒါက loosely coupled ၿဖစ္သြားလို.ပါ။

Untestability ဒါကေတာ့ ရွင္းပါတယ္ unit test ေရးလို. အဆင္မေၿပတဲ့ code ပါ ။ေနာက္ပုိင္းမွာပုိေခတ္စားလာတာက TDD ပါ(Test Driven Design) ပါ code ေတြကုိ မေရးခင္ unit test code ေတြေရးပါတယ္။ ေနာက္မွ code ကုိေရးပါတယ္။ ၿပီးရင္ testing fail မၿဖစ္ေအာင္ code ကုိ refactored လုပ္ပါတယ္။ ဒီလိုနဲ. code ရဲ. quality ကပိုေကာင္းလာပါတယ္။ unit test လုပ္ၿခင္းအားၿဖင့္ ကြ်န္ေတာ္တုိ.ရဲ. code ကုိမွန္မမွန္ စစ္ခ်င္ရင္ unit testing code ကုိ run လုိက္ရံုပါပဲ။ Major open source software ေတြမွာ unit test code က ပါလာၿပီးသားပါ။ ေနာက္တခုက dyanmic language ေတြဟာ တကယ္တမ္း runမၾကည့္ရင္ compile language ေတြလိုမဟုတ္တဲ့အတြက္ error ကုိ statically မစစ္ႏုိင္ပါဘူး။ဒါေၾကာင့္ dynamic language နဲ.ေရးထားတဲ့ code ေတာ္ေတာ္မ်ားမ်ားၾကီးလာၿပီဆုိရင္ unit test ေတြလိုပါၿပီ။ ကြ်န္ေတာ္တုိ.က class ေတြ အမ်ားၾကီးရိွတဲ့အထဲကုိ class တခုထဲ့လိုက္မယ္ အဲ့ class အတြက္ unit test ကုိေရးမယ္ ၿပီးရင္ class အားလံုးအတြက္ unit test ကုိ run လုိက္လုိ. error ၿဖစ္လာၿပီဆုိရင္ ကြ်န္ေတာ္တုိ. ေရးထားတဲ့ class က error ၿဖစ္တယ္ဆုိတာ သိပါၿပီ။ Testable Code ၿဖစ္ေအာင္ေရးဖုိ.ေတာ့ TDD ကိုေလ့လာပါလို.အၾကံၿပဳပါရေစ။ Responsibility တခုထက္ပိုတဲ့ method ေတြ long method ေတြ tightly coupled သို.မဟုတ္ dependency မ်ားတဲ့ class ေတြ concrete class ေပၚ မွီခုိတဲ့ေကာင္ေတြက test လုပ္ရတာခက္ပါတယ္။ အေပၚက ဥပမာ မွာၿပသြားသလုိပါပဲ။

**Premature Optimization**

Premature Optimization is evil လို. Don Knuth ကေၿပာသြားပါတယ္။ ဘာကိုဆုိလိုခ်င္တာလဲဆုိေတာ့ မလိုအပ္ပဲနဲ. Optimization မလုပ္ပါနဲ.လို.ေၿပာတာပါ။ Optimization ဆုိတာဘာလဲဆုိေတာ့ Program တခုကုိ runtime ၿမန္ေအာင္ သုိ.မဟုတ္ memory အစားသက္သာေအာင္ Program ကုိ ပိုမုိေကာင္းမြန္တဲ့ နည္းေတြသို.မဟုတ္ Algorithmေတြသံုးၿပီး ၿပဳၿပဳင္တာၿဖစ္ပါတယ္။ Optimization လုပ္လုိက္ရင္ တနည္းနည္းနဲ. code ေတြဟာ design ကိုထိခုိက္ႏုိင္ပါတယ္ ဒါေၾကာင့္ မလိုအပ္ပဲနဲ. Optimization ကုိအရင္စလိုမလုပ္သင့္ပါဘူးလို.ဆုိခ်င္တာပါ။ 90/10 Rule ဆုိတာရိွပါတယ္။ Program တခုရဲ. execution time 90 ရာခုိင္ႏွဳန္းက 10 ရာခုိင္ႏွုန္းေလာက္ပဲရိွတဲ့ code ေတြ အေပၚမူတည္တာပါတဲ့ခင္ဗ်ာ.

**Indescriptive Naming**

Programmer အမ်ားစုက naming ကုိဂရုမစုိက္က်ပါဘူး။ Indescriptive Naming ဆုိတာက ဘာကိုေၿပာခ်င္တာလဲဆုိေတာ့ program မွာ နားလည္ရမလြယ္ကူတဲ့ ဖတ္လုိက္တာနဲ.မသိတဲ့ variable name ေတြ class name ေတြ function name ေတြ ေပးတာကုိဆုိလုိတာပဲၿဖစ္ပါတယ္။ Programmer ေတြ အမ်ားစုက code ေရးရတဲ့အခ်ိန္ထက္ code ကို ဖတ္ရတဲ့အခ်ိန္က ပိုကုန္ပါတယ္။ ဒါကို Project ၾကီးၾကီးေတြမွာ maintenance လုပ္ရရင္ပိုသိသာပါတယ္။ variable ေတြကိုနာမည္ေပးတဲ့ေနရာမွာ standard မက်တာေတြ အတုိေကာက္ေတြ ဘံုနာမည္ေတြနဲ.ဆုိ အေတာ္ကိုဖတ္ရခက္ပါတယ္။ ဥပမာ C, PHP library ေတြမွာရိွတဲ့ strcmp လုိေကာင္မ်ိဳးပါ။ C ေခတ္ကေတာ့ library အေတာ္နည္းတဲ့အတြက္ သိပ္ၿပႆ နာမဟုတ္ေပမဲ့ ဒီဘက္ေခတ္မွာေတာ့အဆင္မေၿပပါဘူး။ class တခုတည္းမွာ ဆင္တူရုိးမွား method နာမည္ေတြ ဆယ္ဂဏန္းေက်ာ္ေက်ာ္ေပးထားတဲ့ programmer တေယာက္ကုိ ၿမင္ဖူးပါတယ္။ သူ. code ကုိသူပဲ maintenance လုပ္ရေတာ့ ဘယ္ method က ဘာဆုိတာ ထုိင္စဥ္းစားရင္းနဲ. ႏွစ္ေပါက္ေအာင္ အခ်ိန္ကုန္ေနတာကို ေတြ.ဖူးပါတယ္။ ေနာက္တခုက descriptive name ေတြေပးရမဲ့အၿပင္ method တခုမွာ line ကို ဥပမာ static language ေတြမွာဆုိ line 20 maximum dynamic language ေတြမွာဆုိ 10 line ေလာက္ပဲေရးသင့္ပါတယ္ မဟုတ္ရင္ long code ေတြၿဖစ္လာရင္ variable ေတြမ်ားလာမယ္ မွတ္ရတာမ်ားလာမယ္ ေနာက္ၿပီး control structure if ေတြက အစက ဟုိး line 10 ေလာက္မွာ အပိတ္က line 200 ေက်ာ္ေလာက္မွာ ဒါမ်ိဳးကုိ လုိက္ၾကည့္ရတာ ဖတ္ရတာ အေတာ္ စိတ္ပ်က္စရာေကာင္းပါတယ္။ Quality code ဆုိတာ self documented ၿဖစ္ရပါမယ္။ ဥပမာ documentation သို.မဟုတ္ comment ကုိဖတ္စရာမလိုပဲနဲ. ဒီ program ဟာ ဘာလုပ္လဲဆုိတာ သိေလေကာင္းေလပါပဲ literate programming ဆုိတာရိွပါတယ္။ ေလ့လာၾကည့္ေစလုိပါတယ္။ ေနာက္ၿပီး open source software ေတြရဲ. code ေရးသားပံုကုိလည္း ေလ့လာေစခ်င္ပါတယ္။

**Duplication**

Duplication ကေတာ့ အလြယ္တကူသိႏုိင္မွာပါ။ Code ေတြ class ေတြကုိ ဟုိက ဟာကုိ ဒီကုိကူး ဒီက ဟာကုိ ဟုိကုိကူးပါ။ Copy paste ကုိသံုးေနရၿပီဆုိရင္ ဒါဟာ bad programmer ၿဖစ္ေနၿပီဆုိတာကိုသိသင့္ပါတယ္။ Duplicate code ေတြဟာ ထပ္ေနတဲ့အတြက္ တေနရာကို ၿပင္မယ္ဆုိရင္ ေနာက္ကူးထားတဲ့ေနရာမွာလဲ လုိက္ၿပင္ရမွာၿဖစ္တဲ့အတြက္ maintenance ကုိခက္ေစပါတယ္။ ေနာက္ error rate ကုိလဲပိုမ်ားေစပါတယ္။ ခုေခတ္က programming က internet သံုး Google ေခါက္ stackoverflow ကေန copy paste လုပ္ေတာ့ပိုဆုိးပါတယ္။ ကိုယ္ပုိင္ code မဟုတ္ပဲ သူမ်ား code ကုိ copy သံုးတဲ့အတြက္ side effect ဘာရိွမယ္ ဘာေၾကာင့္သံုးရမယ္ဆုိတာ မသိေတာ့ပဲ ဒါေလးထဲ့လိုက္ေတာ့ အလုပ္လုပ္တယ္ေလ ဆုိၿပီး သံုးၾကတာမ်ိဳးေတြပါ။ တကယ္တမ္း maintenenace လုပ္ေတာ့ အဲ့လို code ေတြက error ၿဖစ္ၾကပါတယ္။ Duplicated code ၿဖစ္ၿပီဆုိရင္ ဘံု method classes ေတြ ခြဲထုတ္ၿပီး method ေတြ classes ေတြ ယူသံုးတဲ့နည္းနဲ. refactoring လုပ္ၿပီး ရွင္းသင့္ပါတယ္။
