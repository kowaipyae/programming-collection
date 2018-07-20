## Gentle Introduction to Object Oriented Programming - Part 2
### Inheritance

OO paradigm မွာမပါမၿဖစ္တဲ့ေနာက္ feature တစ္ခုက Inheritance ပါ။ Inheritance ကဘာလုပ္ေဆာင္မွု.ေတြကုိခြင့္ေပးသလဲဆုိေတာ့ existing class တခုကေန code reuse သို.မဟုတ္ နဂိုမူလရိွတဲ့ base class ကုိ extend လုပ္ၿပီး functionality ကုိ modify လုပ္တာၿဖည့္စြက္တာေတြကို ခြင့္ေပးပါတယ္။ Inheirtance ကုိသံုးၿပီး နဂိုမူရင္း base class ရဲ. source code ကိုမထိပဲ ၿပင္လို.ရႏုိင္ပါတယ္ (extend လုပ္ၿပီးေပါ့)။အဲ့လို non-destructive modification ေတြဟာ modern software development မွာမၿဖစ္မေနကုိလုိအပ္ပါတယ္။ Modified class ကို base class ေနရာမွာသံုးလို.ရတာေၾကာင့္ software maintenance ကုိပိုမုိလြယ္ကူေစပါတယ္။ Inheritance ရဲ. major usage က ၂ခုရိွပါတယ္ design မွာသံုးလုိ.ရသလို implementation အတြက္လဲသံုးပါတယ္။ အဲ့ဒါေတြကေတာ့ Inheirtance as conceptual modelling Inheritance as incremental program modification

OOP ရဲ.တၿခား paradigm ေတြထက္ popular ၿဖစ္ရတဲ့အေၾကာငး္ရင္းက Object Orientation ဟာ implementation သက္သက္သာ မဟုတ္ပဲနဲ. modelling or design အတြက္ပါသံုးလို.ရလုိ.ၿဖစ္ပါတယ္။ Real world problem ေတြကို OO thinking နဲ. model ခ်တဲ့အခါမွာပိုမိုလြယ္ကူပါတယ္။ လူေတြဟာ အရာ၀တၳဳေတြ အေၾကာင္းအရာေတြကို ခြဲၿခားစိတ္ၿဖာတယ္ (classification ဥပမာ လူဆုိတာ သတၱ၀ါ တိရစၦာန္ကလဲ သတၱ၀ါ) ၊ generalization (ဥပမာ car engine ကလဲစက္ motor engine ဆိုတာလဲ စက္)၊ grouping,composition အစရိွတာေတြနဲ.ေတြးေခၚၾကပါတယ္။ ခုနကေၿပာတဲ့ classification၊ generalization၊ specialization အစရွိတာေတြကုိ OO paradigm မွာ easiliy model လုပ္လုိ.ရပါတယ္။ classification ကို class contruct နဲ.လုပ္ၾကပါတယ္။ Generalization နဲ. Specialization ကိုေတာ့ inheritance နဲ. model လုပ္ၾကပါတယ္။ Grouping နဲ. composition ကုိေတာ့ class ေတြမွာ တၿခား classes ေတြရဲ. reference variable ေတြထဲ့သြင္းၿခင္းအားၿဖင့္ သံုးၾကပါတယ္။

### Inheritance as conceptual modelling

Inheritance ကို Generalization, Specialization အတြက္သံုးၿပီဆုိရင္ ဒါဟာ inheritance as coneptual modelling ပါ။ Base class or parent class ကို generalized classes လို.ေခၚၿပီးေတာ့ child class ကိုေတာ့ specialized class လို.ေခၚပါတယ္။ Conceptual modelling လုပ္မယ္ဆုိရင္ base class နဲ. drived class ဟာ taxonomy အရတူရမွာပါ။ ဥပမာ Teacher, Doctor နဲ. Human ဆုိတာဟာ taxonomy အရတူပါတယ္။ Hierarchical relationship ရွိတာကိုေၿပာခ်င္တာပါ။ Teacher, Doctor သည္ is a kind of Human ပါပဲ။ Taxonomy အရ မတူဘူးဆုိရင္ Generalization Specialization မလုပ္သင့္ပါဘူး ဥပမာ Bird နဲ. Aeroplane သည္ ပ်ံတာခ်င္းတူေပမဲ့ သူတုိ.ကို Inheritance နဲ.ခ်ိတ္လို.မရပါဘူး။ သူတုိ.က taxonomy အရမတူပါဘူး။ Inheritance လို conceptualization လုပ္ေပးႏုိင္တဲ့ေနာက္တခုက ေတာ့ Subtyping ပါ။Subtyping ဆိုတာ programming lanaugag ကေနေပးထားတဲ့ feature ေတြကုိသံုးၿပီး type တခု သည္ အၿခား type တခုရဲ. subtype ၿဖစ္ပါတယ္ဆုိၿပီးသံုးတာပါ။ Base type ေနရာမွာ based type ကုိအေၿခခံထားတဲ့ တၿခား type ကုိအစားထိုးၿပီးသံုးလို.ရပါတယ္။ Subtyping ကို type polymorphism လို.လဲသံုးၾကပါေသးတယ္ ။ Java, C# တို.မွာဆုိရင္ interface construct ကိုထဲ့ေပးထားပါတယ္။ သူ.ကုိထဲ့ေပးထားရတဲ့အေၾကာင္းရင္းက conceptual modelling အရ taxonomy မတူတဲ့ေကာင္ေတြကုိ polymorphic လုပ္ခ်င္ရင္သံုးဖုိ.ပါ။ Java programmer ေတာ္ေတာ္မ်ားမ်ား က abstract class နဲ. interface ဘာကြာလဲေမးလိုက္ရင္ ေရေရရာရာကဲြၿပားတဲ့အေၿဖကို မေၿဖႏိုင္ၾကပါဘူး။ အဓိက ကြာၿခားခ်က္က taxonomy တူမယ္ဆုိရင္ abstract class ကိုသံုးၿပီး inheritance နဲ.ေၿဖရွင္းမယ္ မတူဘူးဆုိရင္ subtyping ကုိ သံုးၿပီၤး interface နဲ. design လုပ္ရမွာပါ။ ဥပမာ work ဆုိတဲ့ method ကို polymorphic ၿဖစ္ေအာင္လုပ္ခ်င္တယ္ဆုိပါစုိ. Teacher မွာေရာ Doctor မွာေရာ လုပ္ခ်င္တာဆုိရင္ သူတုိ. ၂ခုဟာ taxonomy အရတူတဲ့အတြက္ abstract class ဒါမွမဟုတ္ ရိုးရိုး class သံုးၿပီး inheritance နဲ. model လုပ္ရမွာပါ။ Fly ဆုိတဲ့ method ကို Bird နဲ. Aeroplane အတြက္ polymorphism လုပ္ခ်င္တယ္ဆုိရင္ သူတုိ. ၂ ခုဟာ taxonomy မတူတဲ့အတြက္ Flyable ဆိုတဲ့ interface တခုထားၿပီး model လုပ္ရမွာပါ။ Static type language ေတြမွာ polymorphic operation ေတြလုပ္ဖုို. subtype ေတြၿဖစ္မွ လုပ္လို.ရပါတယ္။ Subtype မဟုတ္ရင္ method ရိွေနလဲ ေခၚလို.မရပါဘူး။ Dynamic language ေတြမွာ duck typing ကိုေပးထားတဲ့အတြက္ အဲ့လိုေခၚလို.ရပါတယ္။ ဒါေပမဲ့ PHP လို dynamic language ၿဖစ္တယ္ duck typing ရတဲ့ language မွာ interface ကိုထဲ့ေပးထားတာဟာ conceptual modelling အရ subtyping ကုိသံုးေစခ်င္လို.ၿဖစ္ပါတယ္။ ေနာက္တခုက normal class နဲ. abstract class ဘယ္လို usage ခြဲမလဲေပါ့ ။ Parent ကေနပဲ child က code ေတြကို one direction ေခၚခ်င္ရင္ hook အေနနဲ.ထားခ်င္ရင္ abstract class ကုိသံုးပါတယ္ မဟုတ္ရင္ both direction ေခၚခ်င္ရင္ေတာ့ normal class ကိုသံုးၿပီး model လုပ္လုိ.ရပါတယ္။

### Inheritance as incremental program modification

Inheritance as incremenatal program modification ဆိုတာ base class ရဲ. source code ကုိမၿပင္ပဲနဲ. သူ.ကို implementation အရ ၿပင္ခ်င္တဲ့အခါမွာ extend လုပ္ၿပီးသံုးတာမ်ိဳးပါ။ ဥပမာ Java မွာဆုိ window frame တခုေဆာက္ခ်င္ရင္ JFrame ကုိ extend လုပ္တာမ်ိဳးပါပဲ။ ဒါကေတာ့ implementation အတြက္သံုးတာပါ။ တခါတေလမွာကုိၿပင္ခ်င္တဲ့ source code ကိုမရႏုိင္လို. binary class file ပဲရတဲ့အတြက္ သူ. functionality ကုိ reuse လုပ္ခ်င္တာၿဖစ္ၿဖစ္ modify လုပ္ခ်င္တာၿဖစ္ၿဖစ္သံုးတာမ်ိဳးကိုလဲ ဒီနည္းထဲမွာအက်ံဳး၀င္ပါတယ္။ Modification ကုိေပးတဲ့ေနရာမွာ language တခုနဲ.တခုမတူပါဘူး။ Inheritance breaks Encapsulation ဆုိတာလဲရိွပါတယ္။ ဘာကိုဆုိခ်င္တာလဲဆုိေတာ့ inheritance ကုိသံုးတာလြဲခဲ့ရင္ သူဟာ parent classes ရဲ. function ေတြကို တလြဲသံုးမိရင္ encapsulation ဆုိတာကို ခ်ိဳးေဖာက္တာၿဖစ္ႏုိင္ပါတယ္။ သတိထားရမွာက parent classes ရဲ. encapsulation ကုိမထိေအာင္သံုးရမွာပါ။ Favour inhertiance over composition ဆုိတာလဲရိွပါေသးတယ္။ တခ်ိဳ.က code reuse လုပ္ခ်င္ယံုသက္သက္နဲ. inheritance ကုိသံုးၾကပါတယ္ ။ taxonomy အရ မတူရင္ေသာ္လည္းေကာငး္ modifcation or added functionality မထဲ့ႏိုင္ရင္ေသာ္လည္းေကာင္း အဲ့လိုသံုးတာမွားပါတယ္။ Code reuse လုပ္ခ်င္ရင္ composition ကုိသံုးပါ။ ဘာလုိ.လဲဆုိေတာ့ inheritance hierarchicy မ်ားလာတာနဲ.အမွ် classes ေတြဟာ dependency မ်ားလာပါတယ္။ Base class တခုကို ေၿပာင္းလုိက္တာနဲ. ေအာက္က child classes ေတြမွာပါ effect ၿဖစ္ႏိုင္ပါတယ္။ Composition ဆုိတာက ကိုသံုးလို.တဲ့ class ကုိ reference variable သံုးၿပီး ယူသံုးတာပါပဲ။

### Single Inheritance vs Multiple Inheritance

C++ မွာေတာ့ multiple inheritance ကုိ support လုပ္ပါတယ္။ Class တခုဟာ တခုထက္ပိုေသာ Base class ေတြရိွႏုိင္ပါတယ္။ Java,C# တုိ.မွာေတာ့ single inheritance ပဲခြင့္ေပးထားပါတယ္။

### Class Inheritance Versus Prototype Inheritance

Programming language ေတြဟာ inheritance ကို support လုပ္တဲ့ပံုစံခ်င္းမတူပါဘူး။ အဓိက ကြဲၿပားတဲ့ပံုစံ ၂ခုက classical inheritance နဲ. prototypical inheritance ပဲၿဖစ္ၾကပါတယ္။

### Classical Inheritance

Java,C++,C# တို.လို language ေတြမွာ support လုပ္တဲ့ inheritance ပံုစံကုိ classical inheritance လို.သံုးပါတယ္။ ဥပမာ ေအာက္က Java program ဆိုပါစုိ.

class Base { int baseData; }

class Child extends Base { int childData; }

Child object တုိင္းမွာ base class ကရတဲ့ baseData နဲ. child class ရဲ. childData ဆုိၿပီး property 2 ခုရမွာပါ။ Child object တခုေဆာက္တုိင္း သီးၿခား baseData တခုစီရေနမွာပါ။ Parent က property ေတြကုိ child object အတြက္ seperate copy ေပးထားတဲ့သေဘာပါ။ Inheritance with copy semantic လို.ေၿပာလို.ရပါတယ္။ ဒါဟာ classical inheritance ပါ။

### Prototypical Inheritance

JavaScript မွာေပးထားတဲ့ inheritance model က prorotypical inheritance ပါ။

function Base() { this.baseData = []; } function Child() { this.childData = "childdata"; } Child.prototype = new Base();//set up inheritance var c1 = new Child(); var c2 = new Child(); c1.baseData.push(100); console.log(c2.baseData);

အေပၚက program မွာ Child.prototype = new Base(); ဆိုတဲ့ statement သံုးၿပီး prototype chain ကို setup လုပ္ပါတယ္ meaning ကေတာ့ child ရဲ. parent သည္ new Base() (Base object) တခုၿဖစ္ပါတယ္ ဆိုတာပါပဲ။ Classical inheritance မွာ parent သည္ class တခုၿဖစ္ေပမဲ့ prototypcial inheritance မွာေတာ့ parent သည္ object တခုၿဖစ္ပါတယ္။ အဲ့ဒီအၿပင္ child object c1 နဲ. c2 ဟာ parent object တခုတည္းကို share လုပ္သံုးရပါတယ္။ ေအာက္ဆံုးအေၾကာင္းမွာထုတ္ထားတဲ့ c2.baseData ဆိုရင္ [100] လုိ.ေတြ.ရမွာပါ။ တကယ္ change လိုက္တာက c1 ရဲ. baseData ကို ေၿပာင္းလိုက္တာပါ။ ဒါေပမဲ့ c1 ေရာ c2 ေရာက same parent object တခုတည္းကုိ share သံုးရတဲ့အတြက္ c2.baseData ဆိုရင္လဲ [100] လို.ထြက္ပါတယ္။ ေအာက္က statement ေလးကို တခ်က္ၾကည့္ပါ

c1.baseData.push(100); ဒါက c1 ဟာ parent ရဲ. baseData ကုိ read access လုပ္တာပါ။ JavaScript ရဲ. inheritance model ကနည္းနည္းရွဳပ္ပါတယ္။

တကယ္လို.မ်ား

c1.baseData = [200]; လို.ေရးလုိက္ရင္ c1 မွာ သူ.ရဲ.ကုိယ္ပုိင္ baseData ဆိုတဲ့ attribute ကို JS ကထဲ့ေပးေတာ့မွာပါ။ Attribute ေတြကို JS မွာရွာတဲ့ပံုစံက read ဆိုရင္ current object ကေန ရွာပါတယ္။ ေနာက္မေတြ.ရင္ သူ. prototype chain ကုိလုိက္ရွာပါတယ္။ တကယ္လို. write သာလုပ္မယ္ဆုိရင္ parent မွာရိွေနလဲ သူ.current object မွာမရိွရင္ attribute အသစ္အေနနဲ.ထဲ့ေပးမွာပါ။ ဒါကုိသတိထားေစခ်င္ပါတယ္။ Prototypical inheritance သည္ share semantic ၿဖစ္ပါတယ္။ Parent object ထဲကုိ attribute ေတြ ထပ္ထဲ့တာ ႏွုတ္တာ အားလံုးသည္ child အားလံုးမွာ effect ၿဖစ္ပါတယ္။

### Dynamic Inheritance

Prototypical inheritance ေပးတဲ့ language ေတြမွာ parent object ကုိ dynamically ေၿပာင္းလို.ရပါတယ္။ ဒါကုိ dynamic inheritance လို.ေခၚပါတယ္။ state အေၿပာင္းအလဲေပၚမူတည္ၿပီး လုပ္ရတဲ့ code ေတြမွာဆုိ Dynamic Inheritance ဟာ အသံုး၀င္ပါတယ္။
