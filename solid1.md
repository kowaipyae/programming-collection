## SOLID Principles - Part 1
ဒီတေခါက္ ကေတာ့ OO Design မွာအေၿခခံအက်ဆံုး principle လို.ဆုိရမဲ့ SOLID ပါ။ SOLID ကိုလူသိမ်ားလာေအာင္ လုပ္ခဲ့တဲ့သူေတာ့ Uncle Bob လုိ.လူသိမ်ားတဲ့ Robert C Martin ပါ။ သူေရးခဲ့တဲ့ စာအုပ္ေတြထဲက ထင္ရွားတဲ့တအုပ္ကေတာ့ Clean Code ပါ။ SOLID က principle တခုတည္းမဟုတ္ပဲ ၄ ခုကိုစုေပါင္းထားတာပါ။ အဲ့ဒါေတြက

 - SRP (Single Responsibility) 
 - OCP (Open Close Principle) 
 - LSP(Liskov Substitution Principle) 
 - ISP(Interface Segregation Principle) 
 - DI(Dependency Inversion)

တုိ.ပဲၿဖစ္ပါတယ္။

### SRP (Single Responsiblity)

ပထမဆံုး principle က အရုိးရွင္းဆံုးနဲ. သံုးရတာ လက္အ၀င္ဆံုး principle ပါ။ သူ.ရဲ. definition ကေတာ့ The Single Responsibility Principle (SRP) states that each software module should have one and only one reason to change. Class တစ္ခု သို.မဟုတ္ module တခုဟာ အေၾကာင္းရင္းတခုေၾကာင့္ပဲ code ကို changes လုပ္ရမယ္။ ဒီေနရာမွာ class or module ရဲ. responsibility ဆုိတာ သူလုပ္ရမဲ့ behaviour(set of method) ကိုဆုိခ်င္တာပါ။ ဆုိခ်င္တာက class, module ေတြဟာ တူညီတဲ့ behaviour ေတြကို စုထားတာပဲၿဖစ္ရမယ္ လို.ဆုိခ်င္တာပါ။ တူညီတဲ့ responsibility ေတြကိုပဲစုထားရမယ္ ဒါမွမဟုတ္ responsibility တခုတည္းကိုပဲ အာရံုစုိက္ရမယ္ လုပ္ရမယ္လို.ဆုိခ်င္တာပါ။ Robert C Matrin ရဲ.ဥပမာ အတုိင္းပဲ ၿပပါမယ္။ ေအာက္က class ကုိၾကည့္ပါ။

    public class Employee 
    { 
    public Money calculatePay(); 
    public void save(); 
    public String reportHours(); 
    }

ၿပထားတဲ့ class မွာ responsiblitiy 3 ခုပါေနပါတယ္။ ဒီအတုိင္းၾကည့္ရင္ တခုတည္းထင္ရေပမဲ့ calculatePay ဆုိတာ accounting နဲ.ဆုိင္တာပါ။ save ကေတာ့ database operation နဲ.ဆုိင္တာပါ။ reportHours() ကေတာ့ HR နဲ.ဆုိင္တာပါ။ ၿပင္ပ realworld က အဲ့ဒီ responsibility ေတြနဲ. တိုက္ရုိက္သက္ဆုိင္တဲ့ entity (ဒီေနရာမွာ calculatePay သည္ HR accounting, save သည္ database, reportHours သည္ HR, management) ေတြသည္ မတူပါဘူး။ ဒါေၾကာင့္ Employee class သည္ single responsiblity ကိုခ်ိဳးေဖာက္ေနပါတယ္။ ၿမင္သာေအာင္ေၿပာရမယ္ဆုိရင္။ Database ကုိေၿပာင္းမယ္ဆုိလဲ (ဥပမာ Employee Table structure ေၿပာင္းသြားလုိ.ဆုိပါေတာ့ ) Employee class ကုိၿပင္ရမယ္။ Payment ေတြေၿပာင္းသြားတယ္ဆုိရင္လဲ Employee class ကိုၿပင္ရမယ္ ဒါဆုိရင္ reason of change သည္ တခုထက္ပိုေနပါၿပီ ဒါဆုိရင္ single responsibility နဲ.မကိုက္ေတာ့ပါဘူး။ Single Responsiblity နဲ.မကိုက္ေတာ့ ဘာၿဖစ္လဲဆုိေတာ့ Cohesion နည္းပါတယ္။ Cohesion နည္းေတာ့ သူ.ကုိ resuse လုပ္ဖုိ.အဆင္မေၿပပါဘူး။ ဥပမာ တၿခား module တခုကေန Employee data ကိုပဲသံုးခ်င္တယ္ pay တြက္တာ မလိုခ်င္ဘူးဆုိရင္ Employee ကုိ reuse လုပ္ဖုိ.အဆင္မေၿပပါဘူး။ ေနာက္တခုက responsibility ေတြေရာေနတဲ့အတြက္ maintenance လုပ္ရတာခက္ပါတယ္။ အဆင္မေၿပပါဘူး။ ဒါေၾကာင့္ ေနာက္ပိုင္း JavaEE Framework ေတြၿဖစ္တဲ့ spring framework လုိေကာင္မ်ိဳးေတြမွာ layer ခြဲၿပီးေတာ့ domain model ကုိသက္သက္ (ဒီေနရာမွာ Employee နဲ.ဆုိင္တဲ့ အခ်က္အလက္ကုိပဲသိမ္းမယ္)။ ေနာက္ service layer (ဒီေနရာမွာ pay calculation နဲ. reportHour ကုိလုပ္မယ္) ေနာက္ DAO layer(ဒီေနရာမွာ Employee object ကို database မွာ save တာကိုလုပ္မယ္ )ဒါမ်ိဳးေတြခြဲလုပ္ၾကပါတယ္။ အဲ့လုိခြဲလုပ္ေတာ့ တခုခုကုိ ၿပင္ခ်င္ရင္ ေနာက္တခုကုိသြားမထိပါဘူး။ ဥပမာ view layer ကုိၿပင္တာနဲ. database layer ကုိသြားထိစရာမလိုပါဘူး။ အဲ့ဒါမ်ိဳးကိုက်ေတာ့ seperation of concern လို.သံုးပါတယ္။ Concern ဆုိတာကေတာ့ system တစ္ခုကုိ feature ေတြ အေပၚမူတည္ၿပီး ခြဲတာပါ။ Feature ဆိုတာကေတာ့ (domain, service, controller, view,database) အဲ့လို feature ေတြ ေပၚမူတည္ၿပီး ခြဲပစ္တာပါ။

ေနာက္ၿမင္ႏုိင္တဲ့ Example တခုကေတာ့ begineer PHP example ေတြမွာေတြ.ရတဲ့ code ေတြပါပဲ။ Business logic နဲ. view (html markup, CSS etc) စတာေတြကုိ ေရာေရးတာပါပဲ။ ေနာက္ပိုင္း framework ေတြမွာေတာ့ တခုခ်င္းကို MVC သံုးၿပီး seperation of concern နဲ.ခြဲထုတ္လုိက္ပါတယ္။ အက်ိဳးဆက္ကေတာ့ better maintenance ၿဖစ္ပါတယ္။

ေနာက္ VB program ေတြမွာေရးေလ့ရိွပါတယ္။ Button တခုရဲ. OnClick event မွာ တခါတည္း database ကိုတန္းခ်ိတ္တာေရာ business logic ေပါင္းေရးတာမ်ိဳးေရာပါ။ အဲ့လိုဆုိရင္ single responsibility ကုိခ်ိဳးေဖာက္ရာက်ပါတယ္။ ဒါဆုိ maintenance လုပ္ရတာအဆင္မေၿပပါဘူး။

Single Responsiblity နဲ.ေၿပာင္းၿပန္ anti pattern ကေတာ့ God Object ပါ ။ God Object ဆုိတာ object, class တစ္ခုမွာ ရိွသမွ် responsiblity ေတြ method ေတြ function ေတြစုေရးထားတာကိုေၿပာတာပါ။ ဒါမ်ိဳးက maintenance လုပ္ရတာ အလြန္ခက္တဲ့အတြက္ မသံုးသင့္ပါဘူး။ SRP ဟာ class module ေတြမွာပဲအသံုး၀င္တာမဟုတ္ပါဘူး method level, code block level မွာသံုးလဲရပါတယ္။ ဥပမာ method တခုဟာ responsibility တခုထက္ပိုေနၿပီဆုိရင္ ထပ္ခြဲထုတ္ (refactoring နည္းနဲ. method အသစ္ၿပန္ထပ္ထဲ့တာမ်ိဳး )လုပ္ရမွာပါ။

### OCP (Open Close Principle)

OCP ကေတာ့ open of extension ,close for modification ကို ရည္ညႊန္းတာပါ။ Class, module code ေတြဟာ လြယ္လြယ္ကူကူ functionality ေတြထပ္ထဲ့ႏုိင္ရမယ္ (open for extension) ဒါေပမဲ့ သူတုိ.ကုိ code modification လုပ္စရာမလုိပဲနဲ. (close for modification) ၿဖစ္ရမယ္လုိ.ဆုိခ်င္တာပါ။ ဥပမာနဲ.ၿပပါမယ္။ ကြ်န္ေတာ္တုိ.က Shape ေတြရဲ. sum area ကုိတြက္ပါမယ္။ Shape ကေလာေလာဆယ္မွာ Circle,Rectangle ဆိုပါစို.ဒါဆုိ pseudo code အေနနဲ.ဆုိဒီလိုရပါမယ္။

    public long sumArea(List<Shape> shapes) 
    { 
    long totalArea = 0; 
    for(Shape s : shapes) 
    { 
    if(s instanceof Circle) 
    { Circle c = (Circle)s; totalArea += c.area(); 
    } 
    else if(s instanceof Rectangle) 
    { Rectangle r = (Rectangle) s; 
    totalArea += r.area(); } 
    } return totalArea; 
    }

အေပၚကေပးထားတဲ့ method မွာ shape ေတြကို loop ပတ္ၿပီး တခုခ်င္းစီကုိ စစ္ပါတယ္ ။ Circle ဆုိ Circle, Rectangle ဆုိ Rectangle အေနနဲ. typecast လုပ္ၿပီး area ေတြကိုေပါင္းပါတယ္။ အဲ့မွာ ဘာၿပႆ နာရိွလဲဆုိေတာ့ close for extension ၿဖစ္ေနတာပါ။ ဆုိခ်င္တာက ကြ်န္ေတာ္က ေနာက္ထပ္ Shape အသစ္ area ကိုတြက္ခ်င္တယ္ Cube ဆုိပါေတာ့ဒါဆုိရင္ ခုနက method sumArea ရဲ. for loop ထဲမွာ if တေၾကာင္းထဲ့ၿပီး type cast လုပ္ area ကိုေခၚ အဲ့လိုလုပ္ရမွာပါ။ ဘာလုိ.လဲဆုိေတာ့ OCP ကုိေဖာက္ဖ်က္လုိ.ပါ။ OCP အတုိင္း ေရးမယ္ဆုိရင္ ဒီလိုရမွာပါ။

    class Shape//base class 
    { long area(); } 
    class Circle extends Shape 
    { long area(){}; } 
    class Rectangle extends Shape 
    { long area(){}; } 
    class Cube extends Shape 
    { long area(){}; } 
    class AreaSummer 
    { 
	    public long sum(List<Shape> allShape) 
	    { 
	    long totalArea = 0; 
		    for(Shape s : allShape) 
		    { totalArea += s.area(); //Here is the point of OCP using, polymorphism } 
	    } 
    }

အေပၚက AreaSummer class ဟာ OCP ကုိလိုက္နာပါတယ္ သူ. loop ထဲမွာ polymorphism ကုိသံုးၿပီး s.area ဆုိၿပီးေခၚပါတယ္။ ဒါဆုိရင္ ကြ်န္ေတာ္တုိ.က ေနာက္ထပ္ shape တခုကိုထပ္ထဲ့မယ္ သူ. area ကိုေပါင္းမယ္ဆုိ ရင္ AreaSummer ရဲ. sum method ကုိၿပင္စရာမလုိေတာ့ပါဘူး။ ဥပမာ Square class ကိုတြက္ခ်င္ရင္ Sqaure class ကို base class Shape ကေန extend လုပ္ၿပီး area method ကုိ override လုပ္ေပးလုိက္ယံုပါပဲ။ ဒါဆုိရင္ ရိွၿပီးသားမူရင္း code ကုိလဲမထိပဲနဲ. ကိုလုိခ်င္တဲ့ functionality (extension ) ကုိလဲ ထပ္ထဲ့ႏုိင္တဲ့အတြက္ OCP နဲ.ကိုက္ညီပါၿပီ။ OCP နဲ.ကိုက္ေအာင္ေရးမထားဘူးဆုိရင္ code ေတြဟာ တခုခု ထပ္ထဲ့မယ္ဆုိရင္ လိုက္ change ေနရပါလိမ့္မယ္။
