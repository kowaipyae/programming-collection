## Calling JavaScript Function in Global Scope

Global Scope မွာေရးထားတဲ့ JavaScript Function တစ္ခုကုိ ဘယ္ႏွနည္းနဲ.ေခၚလို.ရႏုိင္ပါသလဲ ?

    function hello()  
    {  
    console.log("JavaScript");  
    }

    hello();  
    hello.call();  
    hello.apply();  
    hello.bind()();

    this.hello();  
    this.hello.call();  
    this.hello.apply();  
    this.hello.bind()();
    
    this["hello"]();  
    this["hello"].call();  
    this["hello"].apply();  
    this["hello"].bind()();
    
    window.hello();  
    window.hello.call();  
    window.hello.apply();  
    window.hello.bind()();
    
    window["hello"]();  
    window["hello"].call();  
    window["hello"].apply();  
    window["hello"].bind()();

    new hello();  

ဒါကေတာ့ () parenthesis မပါပဲ call တဲ့နည္းပါ။  

    new hello;

ေနာက္ getter,setter ေတြသံုးၿပီး ေခၚမယ္ဆုိလဲ () parenthesis မပါပဲသံုးလုိ.ရႏုိင္ပါတယ္

    var obj = {  
    get hello()  
    {  
    console.log("Hello");  
    },  
    set hello(arg)  
    {  
    console.log("Hello");  
    }  
    };  
    obj.hello  
    obj.hello = "";  

Object.defineProperty ကုိသံုးရင္လဲ ရပါတယ္ 

Firefox မွာ support ေပးထားတဲ့ __noSuchMethod__ ကုိသံုးရင္ Infinity ၿဖစ္ပါလိမ့္မယ္ (no Such method က မရိွတဲ့ method တခုကိုေခၚရင္ ထအလုပ္လုပ္တယ္ )  

    obj.__noSuchMethod__ = function()  
    {  
    console.log("Hello");  
    }  
    obj.blahBlah()

//Have fun and now claim yourself JS Ninja 

