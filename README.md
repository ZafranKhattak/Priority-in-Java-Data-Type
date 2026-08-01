# Priority-in-Java-Data-Type

* Java's overload resolution priority:

Priority	Conversion Type

* 1️⃣	Primitive widening (int → long) ✅
* 2️⃣	Autoboxing (int → Integer)
* 3️⃣	Varargs
* Since primitive widening has higher precedence than autoboxing, display(long a) is chosen.
