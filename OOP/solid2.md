## SOLID Principles - Part 2

### LSP: Liskov Substitution Principle

LSP ကုိအစၿပဳခဲ့တဲ့သူက MIT က Professor Barbara Liskov ဆုိတဲ့ဘြားေတာ္ပဲၿဖစ္ပါတယ္။ ဘြားေတာ္က ACM Turing Award Winner လဲၿဖစ္ပါတယ္။ ACM Turing Award ဆိုတာ Alan Turing ကို ဂုဏ္ၿပဳၿပီး ေပးထားတဲ့ Computer Science မွာ အၿမင့္ဆံုး ဆုပါပဲ။ Language Designer ေတြ OS Designer ေတြ Computer Science ကုိတနည္းတဖံုေၿပာင္းလဲေပးခဲ့တဲ့သူေတြပဲရၾကပါတာပါ။ Dennis Ritchie (C language Designer) နဲ. Ken Thompson တုိ.လဲ ရဖူးပါတယ္ UNIX ကို သူတုိ.ႏွစ္ေယာက္လုပ္ခဲ့ၾကလို.ပါ။ Liskov က CLU နဲ. Argus ဆုိတဲ့ Programming Languge ၂ခု ရဲ. designer ပါ။ အဲ့ language ေတြက OOP ကုိေၿပာင္းလဲေစခဲ့ပါတယ္။ တခါတေလ ေၿပာေနၾကတဲ့ ငါတုိ. langauge က feature ကုိ ဟုိဘက္က langauge က ခုိးသြားတယ္ဆုိတာမ်ိဳး ၾကားဖူးမွာပါ။ တကယ္ကရီစရာပါ modern language ေတာ္ေတာ္မ်ားမ်ားက သူတုိ.ကုိယ္ပုိင္ concept ဆုိတာထက္ ေရွးက langauge concept ေတြအေပၚထပ္ေကာင္းေအာင္ လုပ္ထားၾကတာပါပဲ။

LSP အႏွစ္ခ်ဳပ္ကေတာ့ ေအာက္ပါအတိုင္းပါပဲ။

> Methods that use references to the base classes must be able to use
> the objects of the derived classes without knowing it

OO မွာ program ေတြဟာ inheritance ကုိသံုးၿပီး class heirarchy ေတြေဆာက္ၾကပါတယ္။ အဲ့ဒီမွာ base class (parent class, super class, super type) ရဲ. reference ကုိသံုးထားတဲ့ေနရာမွာ child class (derived class,subtype, sub class) ရဲ. object ကို child class object သည္ ဘာ class ဆုိတာမ်ိဳး သိစရာမလိုပဲ သံုးလို.ရ ရမယ္လို.ဆုိပါတယ္။ နည္းနည္းထပ္ရွင္းပါဦးမယ္။ parent reference သံုးထားတဲ့ method ေတြမွာ child object ေတြကို parent object ေတြေနရာမွာ အစားထုိးသံုးလုိ.ရရမယ္။ အဲ့လိုသံုးလုိ.ရဖုိ. ဘယ္လုိ knowledge မွမလိုဘူး။ (ဒီေနရာ မွာ knowledge ဆုိတာ part1 ကၿပထားတဲ့ open close principle example မွာၿပထားတဲ့ instanceof operator နဲ.စစ္တာမ်ိဳးကိုပါ)။ ဒါကို LSP Liskov Substitution principle လုိ.ေၿပာပါတယ္။ Subsitution ကဘာကုိဆုိလုိခ်င္တာလဲဆုိေတာ့ child object ေတြသည္ parent refernece သံုးတဲ့ေနရာမွာ ဘာမွအေၿပာင္းအလဲမရိွပဲ သံုးႏုိင္ရမယ္။ child class က object သည္ parent class ေနရာမွာ semantically equalivent အေနနဲ့သံုးႏုိင္ရမယ္။ code သည္ child object ကုိသံုးေနတာလား parent object ကုိသံုးေနတာလားဆုိတာကို သိစရာကိုမလိုဘူး ။ အစားထုိးနုိင္ရမယ္ ဒါကိုေၿပာခ်င္တာပါ။ နဂို parent reference ကုိသံုးထားတဲ့ code ကိုၿပဳၿပင္စရာမလိုပဲ parent reference ေနရာမွာ child object ကုိသံုးႏုိင္ရမယ္။ ဒါမွသာလွ်င္ ေနာက္ထပ္ functionality အသစ္ထဲ့တာလုိေနရာမ်ိဳးမွာ မူရင္း code ကိုမထိပဲၿပင္လို.ရမွာပါ။ extensible ၿဖစ္ေအာင္ ရယ္ maintenance ေကာင္းေအာင္လို.ေၿပာရင္ ရမွာပါ။ LSP သည္ inheritance ကုိ နည္းမွန္လမ္းမွန္သံုးႏုိင္ေအာင္ ၿပထားတဲ့ principle လို.ေၿပာရမွာပါ။ LSP က OCP နဲ.ဆက္စပ္ေနပါတယ္။ LSP ကုိခ်ိဳးေဖာက္ၿပီဆုိရင္ OCP ကုိ ခ်ိဳးေဖာက္သလိုလဲၿဖစ္ႏုိင္ပါတယ္။

Inheritance hierarchy ေတြခ်တဲ့ေနရာမွာ child class (subtype) သည္ parent class (super type) ရဲ. semantic အတုိင္း လုိက္နာရပါလိမ့္မယ္။ ဆုိခ်င္တာက child class မွာ override လုပ္ထားတဲ့ parent ရဲ. method ေတြသည္ paernt ရဲ. nature နဲ. semantically မတူဘူးဆုိရင္ ဒါ LSP ကုိခ်ိဳးေဖာက္တာပါပဲ။ ဒီ https://sanaulla.info/2011/11/28/solid-liskov-substitution-principle-2/ link ကဥပမာေလးကုိၿပင္ၿပီး ေပးပါရေစ ရွင္းလြယ္လုိ.ပါ။

    class Bird 
    { 
	    public void fly(){} 
	    public void eat(){} 
    } 
    class Crow extends Bird {} 
    class Penguin extends Bird
    { 
	    fly()
	    { 
		    throw new UnsupportedOperationException(); // violate LSP here 
		 } 
    } 
    public BirdTest
    { 
	    public static void main(String[] args)
	    { 
		    List<Bird> birdList = new ArrayList<Bird>(); 
		    birdList.add(new Bird()); 
		    birdList.add(new Crow()); 
		    birdList.add(new Penguin()); 
		    letTheBirdsFly ( birdList ); 
	    } 
    static void letTheBirdsFly ( List<Bird> birdList )
	    { 
		    for ( Bird b : birdList ) { b.fly(); 
	    } 
    } 
    }

အေပၚက example မွာ LSP ကုိခ်ိဳးေဖာက္ထားတာကိုၿပထားပါတယ္။ Bird ဆုိတဲ့ class ကေန Crow ရယ္ Penguin ရယ္က extend လုပ္ပါတယ္(subtyping)ေပါ့။ Bird မွာ fly ဆုိတာပါပါတယ္။ Crow ကေတာ့ ပ်ံႏုိင္ပါတယ္ ဒါဆုိ Bird fly ကုိသံုးရင္ သူ. fly ကုိလဲသံုးလို.ရပါတယ္။ Penguin ကေတာ့မပ်ံႏုိင္ပါဘူး ဒါေၾကာင့္ သူ. method မွာ exception ကုိ လႊင့္ခုိင္းလုိက္ပါတယ္။ အဓိက Penguin သည္ မပ်ံႏုိင္ပါဘူး ဒါေၾကာင့္ Bird ရဲ. fly သူ.မွာမရိွတဲ့အတြက္ bird fly ကုိသံုးထားတဲ့ code ေတြမွာ penguin သည္ အလုပ္လုပ္ႏုိင္မွာမဟုတ္ပါဘူး။ ဒါဆုိရင္ ကြ်န္ေတာ္တုိ.ရဲ. b.fly() code ကိုလုိက္ၿပင္ေနရတာမ်ိဳးၿဖစ္ေနပါလိမ့္မယ္။ ဒါက LSP ကုိမလိုက္နာတဲ့အတြက္ OCP ကုိပါ ထိသြားတာကိုၿမင္ႏုိင္ပါလိမ့္မယ္။ LSP ကေပးခ်င္တဲ့ theme ကေတာ့ child class ေတြကို extend လုပ္တဲ့အခါမွာ သူတုိ. method ေတြဟာ parent method ေတြနဲ. အစားထုိးသံုးလို.ရ ရပါလိမ့္မယ္ဆုိတာပါပဲ။

### Interface Segregation principle (ISP)

ဒီ principle ကေတာ့ရွင္းပါတယ္ မလိုအပ္ပဲနဲ. interface ေတြမွာ method ေတြ အမ်ားၾကီးစုၿပံဳထားတာမလုပ္ရဘူးလုိ.ေၿပာခ်င္တာပါ။ အဲ့လို စုၿပံဳထားေတာ့ အဲ့ interface ကုိ implements လုပ္တဲ့ class ေတြဟာ မလိုအပ္ပဲနဲ. တၿခား method ေတြကိုပါ လုိက္ေရးရတာမ်ိဳးပါ။ အဲ့အစား interface ေလးေတြ အမ်ားၾကီး ထပ္ခြဲၿပီး တခုခ်င္းဆီမွာ ဆုိင္တဲ့ method ေလးေတြ ပဲထဲ့သင့္ပါတယ္။ ဒါကလဲ single responsibility (SRP) နဲ.ကိုက္ညီေအာင္ လုပ္လိုက္တဲ့သေဘာပါပဲ။ Fat Interface မလုပ္ပဲနဲ. small interface ေလးေတြပဲခြဲခုိင္းတာပါ။ client class တခုဟာ သူမသံုးတဲ့ သူ.အတြက္မလိုအပ္တဲ့ method ေတြကို fat interface ေၾကာင့္ လုိက္ override လုပ္ေနရရင္ မေကာင္းပါဘူး။

### Dependency Inversion Principle (DIP)

သူ.ရဲ. main rule ၂ခုကေတာ့ေအာက္ပါအတုိင္းပါပဲ။

High-level modules should not depend on low-level modules. Both should depend on abstractions. Abstractions should not depend upon details. Details should depend upon abstractions.

အေပၚက ၂ေၾကာင္းကုိမရွင္းခင္မွာ Abstraction ဆုိတာကိုအရင္ရွင္းရပါလိမ့္မယ္။ Abstraction ဆိုတာ program module သို.မဟုတ္ code ေတြကို detail implementation ကိုသိစရာမလိုပဲ သံုးႏိုင္ေအာင္ အလုပ္လုပ္ႏုိင္ေအာင္ လုပ္ေပးထားတာကို abstraction လုိ.ဆုိခ်င္တာပါ။ All implementation detail ကို client မၿမင္ရေအာင္ abstract လုပ္ထားတာပါ။ အဲ့ေတာ့ implementation ကေၿပာင္းမယ္ဆုိရင္လဲ client အေနနဲ. အဲ့ဒီ changes ကုိသိစရာမလိုေတာ့ဘူးေပါ့ဗ်ာ။

### Depend on Abstraction

အဲ့ေတာ့ depend on abstraction ကုိရွင္းရရင္ class ေတြ code ေတြ module ေတြဟာ concrete class (interface မဟုတ္ abstract class မဟုတ္ေသာ class မ်ား) ေတြ သံုးၿပီး relation မခ်ိတ္ပဲ မသံုးပဲ relationship အားလံုးကို abstract class သုိ.မဟုတ္ interface ကုိသံုးၿပီး model လုပ္တာကိုဆုိခ်င္တာပါ။ အဲ့ေတာ့ ကြ်န္ေတာ္တုိ.က class တခုက တၿခား class တခုကို သံုးဖုိ.လိုၿပီဆုိရင္ concrete class အစား abstract class သုိ.မဟုတ္ interface ကုိသံုးတာက ပုိၿပီး ေကာာင္းတယ္လို.ဆုိခ်င္တာပါ။ ဒါကို depened on abstraction ရဲ.သေဘာေပါပဲ။ ဘာလုိ.လဲဆုိေတာ့ concrete class ကုိသံုးမယ္ဆုိရင္ ကြ်န္ေတာ္တုိ.က သူ. class ရဲ. variable ေတြ implementation detail ေတြကို accidentally ယူသံုးမိႏုိ္င္ပါတယ္။ interface ,abstract class ေတြမွာေတာ့အဲ့လို မရိွႏုိင္ပါဘူး။ ေနာက္ၿပီး interface,abstract class သံုးမယ္ဆုိရင္ သူ.တုိ.ရဲ. dervied class ေတြ implementation ေၿပာင္းလဲ interface method ေတြအေပၚမွာပဲ မူတည္ၿပီး သံုးထားတာၿဖစ္တဲ့အတြက္ code က changes လုပ္စရာမလိုပါဘူး။ဒါက depend on abstraction ရဲ. ေကာင္းက်ိဳးေပါ့ဗ်ာ။ အဲ့ေတာ့ module တခုနဲ.တခုၾကားမွာ inteface ေတြသံုးၿပီးေတာ့ပဲ program dependency ကုိ create လုပ္သင့္တယ္လို.ဆုိလုိတာပါ။ ဥပမာ Java Spring Framework မွာဆုိ DAO, Service layer ေတြမွာ interface ကုိသံုးထားၿခင္းဟာ DI principleအတြက္ depence upon abstraction ကိုလိုက္နာထားတာပါပဲ။

### Dependency

class တခု module တခုက တၿခား class တစ္ခုကုိ reference လုပ္ရၿပီ ယူသံုးရၿပီဆုိရင္ ဒါဟာ dependency ပါပဲ။ ေအာက္က ဥပမာကိုၾကည့္ပါ။

    class Computer 
    { 
	    Mouse mouse; public setMouse(Mouse m) 
		    { this.mouse = m; } 
    } 
    class Mouse 
    { //mouse implementation }

အေပၚက code example မွာ Computer class ဟာ Mouse class ကို ယူသံုးထားပါတယ္ ဒါက dependency ပါ။ ဒါဆုိရင္ ဘာအားနည္းခ်က္ရိွလဲေပါ့ အဲ့ code မွာ Mouse သည္ concrete class ၿဖစ္ပါတယ္ (ဒီေနရာမွာ Java class ေတြက extend လုပ္ၿပီး method ေတြက virtual method ၿဖစ္တာေၾကာင့္ မသိသာပါဘူး C++ မွာဆုိ ရင္ေတာ့သိသာပါၿပီ)။ ဒါေၾကာင့္ ကြ်န္ေတာ္တုိ.က တၿခား Mouse တခုခုနဲ.အစားထုိးဖုိ. အဆင္မေၿပႏုိင္ပါဘူး ဘာလုိ.လဲဆုိေတာ့ကြ်န္ေတာ္တုိ.က Mouse class ရဲ. implementation အေပၚမွာ directly depend ၿဖစ္ေနလို.ပါ။ ဒါဆုိကြ်န္ေတာ္တုိ.က concrete class Mouse အေပၚမွာ တုိက္ရိုက္မမွီခုိပဲ ေအာက္ကလို ေရးလိုက္မယ္ဆုိရင္ ဒါက Dependency Inversion ပါပဲ။

    class Computer 
    { 
	    IMouse mouse; public setMouse(IMouse m) 
	    { this.mouse = m; } 
    } 
    interface IMouse 
	    { //mouse methods} 
	    
    class WirelessMouse implements IMouse {}
    
    class USBMouse implements IMouse {}

အေပၚက code မွာ ပထမ ဥပမာနဲ.မတူပဲ Computer class ဟာ concrete mouse class (WirelessMouse,USBMouse) ေတြအေပၚမွာ direct dependency မရိွေတာ့ပဲ interface IMouse အေပၚမွာပဲ dependence ၿဖစ္သြားပါၿပီ။ Concrete class အေပၚမွာ dependence ၿဖစ္ေနတာကို interface ကုိေၿပာင္းၿပီး dependency ကုိ inverse လုပ္လိုက္တာပါ။ အက်ိဳးဆက္ကေတာ့ကြ်န္ေတာ္တုိ.က Computer class က ၾကိဳက္တဲ့mouse implementation ကုိအစားထုိးသံုးလို.ရတာပါပဲ။ Dependency Inversion နဲ. Dependency Injection ကမတူပါဘူး ဒါေပမဲ့ ဆက္စပ္မွူေတာ့ရိွပါတယ္။ Dependency Inversion က Dependency ေတြကိုေရႊ.တာၿဖစ္ၿပီးေတာ့ Dependency Injection ကေတာ့ Dependence Object ေတြကို Dependency Injection Container တခုသံုးၿပီး system ကေန dependency ေတြကို ထဲ့ေပးတာကိုေၿပာတာပါ။
