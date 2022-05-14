# Increment and Decrement
من العمليات المتكررة أثناء البرمجة، عملية زيادة واحد على قيمة المتغير الحالية أو إنقاص واحد منها. تسمى عملية الزيادة في هذه الحالة Increment وتُسمى عملية الإنقاص Decrement. سنتحدث في هذا الجزء عن طريقة استخدامهما و سنتطرق لشرح مفهوم prefix و postfix الفرق بينهم.

## **مقدمة في Increment و Decrement**

كما ذكرنا سابقا يستخدم Increment لزيادة واحد على قيمة المتغير و يستخدم Decrement لخصم واحد من قيمة المتغير، لتوضيح الفكرة العامة، لاحظ معي الأسطر التالية:

    void main() {
    var number = 5;
    number = number + 1;  
    number = number - 1; 
    }

في السطر الثاني، قمنا بزيادة واحد على قيمة number، لتصبح القيمة 6. وفي السطر الثالث بخصم واحد من قيمة number، لتصبح 5. توفر لغة JavaScript طريقة مُختصرة لتنفيذ كلتا العمليتين السابقتين، وذلك من خلال استخدام معامل الزيادة ++ لزيادة واحد على قيمة المتغير وهذا هو المقصود بمفهوم Increment، ومعامل الخصم -- لخصم واحد من قيمة المتغير وهذا هو المقصود بمفهوم Decrement. لتوضيح الفكرة، دعنا نقوم بإعادة كتابة المثال السابق بالطريقة المُختصرة في المثال التالي:

    void main() {
    var number = 5;
    number++; // increment
    number--; // decrement
    
    }

كما تلاحظ في المثال السابق قمنا باستخدام الطريقة المختصره لكل من عملية الزيادة و الخصم و هذا باستخدام Increment و Decrement
لا يمكن استخدام Increment و Decrement إلا على المتغيرات. عند محاولة استخدامها على الثوابت او قيمة مثل 3++ سيعطي خطأ.


## **مفهوم prefix و postfix**

يمكنك وضع علامة ( Increment أو Decrement ) قبل المتغير أو بعده و هذا سوف يؤثر على توقيت تنفيذ عملية، فمثلا عند وضع العلامة بعد المتغير، فإنها تُسمى postfix، وعند وضعها قبل المُتغير تُسمى prefix. حتى نفهم الفرق بين prefix و postfix، لاحظ معي المثال التالي:

    void main() {
    var number = 2;
    var result = number++ + 4; // postfix
    print(result);
    print(number);
    
    }

في المثال السابق، استخدمنا أسلوب postfix لان ++ أتت بعد number، وهذا يعني أن قيمة number ستزداد بعد تنفيذ العملية الحالية، أي سيتم أخذ القيمة الحالية للمتغير number، وهي 2، ثم سيتم جمعها إلى القيمة 4، ويتم تخزينه في result، وبعد الإنتهاء من تنفيذ هذه العملية، سيتم زيادة واحد على number .أي أن postfix تعني قم “بالزيادة بعد تنفيذ العملية”. ليصبح الناتج هو طباعة التالي:

    6
    3

أما بالنسبة لطريقة prefix، فهي العكس، و هذا يعني أن قيمة المتغير “ تزداد قبل تنفيذ العملية الحالية”. لتوضيح الفكرة، دعنا نقوم بإعادة المثال السابق ولكن بطريقة prefix على النحو الموضح في الأسطر التالية:

    void main() {
    var number = 2;
    var result = ++number + 4; // prefix
    print(result);
    print(number);
    }

في هذه الحالة، سيتم زيادة قيمة number لتصبح 3، وبعد ذلك يتم تنفيذ العملية عليه بجمعه مع 4 لتصبح قيمة result هي 7، و يتم طباعة التالي:

    7
    3

بالنسبة لعملية الخصم -- فينطبق عليها ما ذكرناه عن ++ ، أي أنها تكون على هيئة prefix و postfix، وتختلف في أن العملية هنا عملية خصم،postfix تخصم واحد من المتغير **بعد** تنفيذ العملية عليه، و prefix، تخصم واحد من المتغير **قبل** تنفيذ العملية عليه
تعرفنا في هذا الدرس على عمليت Increment لزيادة واحد لقيمة المتغير و Decrement لخصم واحد من قيمة المتغير وتطرقنا لشرح مفهوم prefix و postfix و الفرق بينهما.

