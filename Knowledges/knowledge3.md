## How C/C++ works

C/C++ ကို system programming, embedded programming, Game programming လိုေနရာေတြမွာမၿဖစ္မေနသံုးရတုန္းပဲ။ ဘာလုိ.လဲဆိုရင္ native speed ရတယ္ hardware ကိုတုိက္ရုိက္ ထိန္းလို.ရတယ္ ဆုိတဲ့အခ်က္ေတြေၾကာင့္ပဲ။ ဥပမာ device driver ေတြေရးမယ္ဆုိရင္ assembly,C , C++ လို low level programming အေနနဲ.ေရးလို.ပဲရမယ္။ High level တၿခား language ေတြကအဆင္မေၿပဘူး။ေနာက္တခုက native speed, native speed ဆုိတာ C/C++ က ထုတ္တဲ့ executable binary code သည္ native platform ဥပမာ Intel CPU, window platform အဲလိုေကာင္ေတြအေပၚမွာ တုိက္ရိုက္ run ႏုိင္တယ္။ 

ဒါေၾကာင့္သူတုိ.သည္ speed အရဆုိရင္ ၿမန္တယ္။ တၿခား language ေတြ ဥပမာ Java,C#, Python, PHP အဲ့ေကာင္ေတြသည္ Virutal machine ဒါမွမဟုတ္ interpreter တခုခုခံေနရတဲ့အတြက္ C/C++ လို မၿမန္ႏုိင္ဘူး။ ၾကားထဲမွာ တဆင့္ခံၿပီးေတာ့ machine code အၿဖစ္ေရာက္ေအာင္ ၿပန္ေၿပာင္းေပးေနရေသးတယ္။ Layer တခု ထပ္ခံရတယ္ေပါ့။ေနာက္တခုက system programming လိုေနရာမ်ိဳးမွာ hardware ကုိ direct ကိုယ္တြယ္ရမယ္ဆုိရင္ C/C++ လုိ မ်ိဳး low level ထိေရးလို.ရတဲ့ (C/C++ မွာ assebmly ကုိ embed လုပ္ေရးရင္လဲရတယ္ ေနာက္တၿခား library ေတြသံုးၿပီးေတာ့ low level device ေတြကို ခုိင္းရင္လဲ ရတယ္) programming language မွပဲအဆင္ေၿပမယ္။

အဲ့ဒီေတာ့ serious programmer (ဆုိခ်င္တာက system programming အထိ Low level ေတြအထိ နားလည္ေအာင္လုပ္ေတာ့မယ္ဆုိရင္ C/C++ သည္ မၿဖစ္မေနကို နားလည္ရမယ္ ) အဲ့လိုမွမဟုတ္ဘူးဆုိရင္ memory ဆုိတဲ့ concept မ်ိဳးကိုေတာင္ တၿခား high level langauge ေတြနဲ.ဆုိရင္ ေသခ်ာနားလည္ေအာင္ ရွင္းၿပလို.မရဘူး။ Address ေတြ pointer ေတြဆိုတာ သူတုိ.မွာ ရိွမွမရိွပဲနဲ.ကိုး

Open Source ရတဲ့ C/C++ compilerေတြမွာ GCC (GNU compiler collection) က နာမည္အၾကီးဆံုးပဲ ။ အဲ့ေတာ့ အဲ့ဒီ ေကာင္ေတြသံုးၿပီး C/C++ ဘယ္လို compile လုပ္သြားသလဲဆုိတာကိုၾကည့္ရေအာင္။

အဓိက အားၿဖင့္ C/C++ ကေန native code(executable code)ထုတ္ေတာ့မယ္ဆုိရင္ ဒီအဆင့္ေတြလုပ္ရတယ္။

**Preprocessing Compiling Assembly Linking**

အဲ့ေကာင္ေတြပါတယ္။ တၿခား Compiler ေတြအေပၚမူတည္ၿပီးေတာ့ အထဲမွာ intermediate representation ေတြကြာတာရိွမယ္။ ေနာက္ Optimization ေတြကြာမယ္။ ဒါေပသိ C/C++ Compiler အမ်ားစုကေတာ့ ခုနက ေလးဆင့္ကို ပါကိုပါရတယ္။

**Preprocessing**

C/C++ program ေတြရဲထိပ္ဆံုးမွာ # နဲ.ခံၿပီးေရးတဲ့ statement ေတြကို preprocessor statement လို.ေခၚပါတယ္ သူတုိ.က အဓိကကေတာ့ marco expansion , code replacement အစရိွတာေတြလုပ္ၾကတာပါ။ Hearder file တခုကိုေခၚထားၿပီဆုိရင္ ဥပမာ #include<stdio.h> လုိ.ေခၚထားရင္ သူ.ထဲကေနသံုးမဲ့ put function ကုိသံုးမယ္ဆုိပါစုိ. ဒါကို externally reference လုပ္ပါတယ္ဆုိၿပီး အစားထိုးလိုက္ပါတယ္။ဥပမာ ဒီ C program ဆုိပါစုိ.

    #include<stdio.h> 
    int main(void) { 
    puts("Hello, World!"); 
    return 0; 
    }

သူ.ကို preprocesor ကေနရွင္းလုိက္ရင္ ဒီလိုၿဖစ္သြားပါလိမ့္မယ္။

    extern int __vsnprintf_chk (char * restrict, size_t, int, size_t, const char * restrict, va_list); 
    # 493 "/usr/include/stdio.h" 2 3 4 # 2 "hello_world.c" 2 int main(void) { puts("Hello, World!"); return 0; }

အေပၚဆံုးက extern နဲ.စတဲ့ေကာင္ေတြသည္ ဒါက external function call လို.ဆုိလုိတာပါ။ stdio library ထဲက ဘယ္ function ကုိယူသံုးမယ္လုိ.ဆုိခ်င္တာပါ။ အဲ့ေတာ့ preprocesor ရဲ.အလုပ္ကို အရိုးဆံုးေၿပာရမယ္ဆုိရင္ library call ေတြကို ထဲ့မယ္။ source expanding လုပ္မယ္။ replacing လုပ္မယ္။ ေနာက္ textual replacement လုပ္မယ္ေပါ့။ အေသးစိတ္ကေတာ့

https://gcc.gnu.org/onlinedocs/cpp/

ဒီမွာသြားၾကည့္ပါ။

ေနာက္တဆင့္ Compilation ေပါ့။ Compilation လို.ဆုိလုိက္ရင္သူက lexical analysis (token ေတြ တခုၿခင္းၿဖတ္ထုတ္တာ ဘယ္ဟာက operator, ဘယ္ဟာက keyword, ဘယ္သူက variable အဲ့တာေတြ သိေအာင္လုပ္တာ) ေနာက္ Syntax Analysis လုပ္ရပါတယ္။ သူကေတာ့ C/C++ grammar rule ေတြနဲ.ေရးထားတဲ့အတုိင္း မွန္ရဲ.လားဆုိၿပီးေတာ့ စစ္ရတာပါ။ ခုနက Lexical Analysis နဲ. syntax analysis အဆင့္ကို font end လို.ေခၚပါတယ္။ Synatx analysis အဆင့္ကေန AST(Abstract Syntax Tree) ထုတ္ပါတယ္။ ခုနက AST ကုိ compiler ေတြအေပၚမူတည္ၿပီးေတာ့ Optimization processing ေတြ လြယ္ေအာင္ တၿခား representation ေတြေၿပာင္းၾကပါေသးတယ္ ။ဥပမာ GCC compiler ေတြမွာဆုိရင္ RTL (Register Transfer Language ) ဆုိၿပီးေတာ့ ေၿပာင္းပစ္ပါေသးတယ္။ RTL က assembly ေလာက္မဟုတ္ပဲနဲ. unlimited register ေတြရတဲ့ abstract register langauge အေနနဲ.ေရးထားတာပါ။ ခုနက RTL ကေနမွ တဆင့္ assembly code ကုိထုတ္ပါတယ္။ ဒါဆုိရင္ ခုနက အေပၚက program ကို Compile လုပ္လုိက္ရင္ ဒီလို assembly ရပါလိမ့္မယ္။

       .section    __TEXT,__text,regular,pure_instructions
        .macosx_version_min 10, 10
        .globl  _main
        .align  4, 0x90
    _main:                                  ## @main
        .cfi_startproc
    ## BB#0:
        pushq   %rbp
    Ltmp0:
        .cfi_def_cfa_offset 16
    Ltmp1:
        .cfi_offset %rbp, -16
        movq    %rsp, %rbp
    Ltmp2:
        .cfi_def_cfa_register %rbp
        subq    $16, %rsp
        leaq    L_.str(%rip), %rdi
        movl    $0, -4(%rbp)
        callq   _puts
        xorl    %ecx, %ecx
        movl    %eax, -8(%rbp)          ## 4-byte Spill
        movl    %ecx, %eax
        addq    $16, %rsp
        popq    %rbp
        retq
        .cfi_endproc
    
        .section    __TEXT,__cstring,cstring_literals
    L_.str:                                 ## @.str
        .asciz  "Hello, World!"
    
    
    .subsections_via_symbols

Assembly သည္ platform တခုနဲ.တခုမတူပါဘူး ဒါေၾကာင့္ C/C++ Compiler ေတြသည္ platform အေပၚမူတည္ၿပီး သင့္ေတာ္တဲ့ assebmly code ေတြထုတ္ေပးရပါတယ္။ ခုနက intermediate code ကေန assembly code ထုတ္တာကို compiler ရဲ. backend လုိ.သံုးပါတယ္။

Assembly code ရလာေပမဲ့ ခုနက assembly code ကို run ဖုိ.အတြက္ assembler နဲ. compile ထပ္လုပ္ရပါတယ္။ ဒါကို assembling လုပ္တယ္လုိ.ဆိုပါတယ္။ Assembler သည္ assembly code ကုိယူၿပီး object code ထုတ္ပါတယ္။ Object code ဆုိတာ ရွင္းေအာင္ေၿပာရရင္ machine code နီးနီးပါပဲ ဒါေပမဲ့ external library ေတြအတြက္က်ေတာ့ သူတုိ.က external symbol reference အေနနဲ.ပဲၿဖစ္ေနပါတယ္။ အဲ့ေတာ့ခုနက assembly code ကုိ assembler နဲ. assemble (compile လုိ.မသံုးဘူး assemble လုိ.သံုးတယ္)လုပ္လုိက္ရင္ object code ရပါတယ္။ အဲ့ဒီ object code မွာ external library call ေတြကုိေခၚထဲ့ဖုိ.က်ေတာ့ linker ကုိသံုးရပါတယ္။ Linker က object code ေတြအကုန္ကိုစုၿပီး (ဆုိခ်င္တာက user program ကေန library ေခၚရင္ user program object code ေရာ library object code ကုိေရာ တခါတည္းစုေပးရတယ္) linking လုပ္ပါတယ္။ Link လုပ္တယ္ဆုိတာ ခုနက object code မွာပါလာတဲ့ symolic reference ေတြကို ဆုိင္ရာ machine code အေနနဲ. အစားထုိးၿပီး executable code ေဆာက္လုိ္က္တာပါပဲ.။ ဒါဆုိရင္ ခု ထြက္လာတဲ့ executable code ကုိ native platform အေပၚမွာ run လို.ရသြားပါၿပီ။

Ref

[https://www.calleerlandsson.com/the-four-stages-of-compiling-a-c-program/](https://www.calleerlandsson.com/the-four-stages-of-compiling-a-c-program/)
