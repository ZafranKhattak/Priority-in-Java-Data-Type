# Priority-in-Java-Data-Type in Method Overloading

* Java's overload resolution priority:

Priority	Conversion Type

* 1️⃣	Primitive widening (int → long) ✅
* 2️⃣	Autoboxing (int → Integer)
* 3️⃣	Varargs
* Since primitive widening has higher precedence than autoboxing, display(long a) is chosen.

# The hierarchy:

* String implements CharSequence
* StringBuilder implements CharSequence
* StringBuffer  implements CharSequence
* String and StringBuilder are siblings (neither is a subclass of the other)
* String is a subclass of CharSequence
* CharSequence is a subtype of Object
* So String is more specific than both CharSequence and Object
