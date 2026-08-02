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
* String and StringBuilder are siblings (neither is a subclass of the other)
* String is a subclass of CharSequence
* CharSequence is a subtype of Object
* So String is more specific than both CharSequence and Object

$ Method selection analysis:
* Method	Is null applicable?	Specificity
* method(String s)	✅ Yes (null can be assigned to String)	Most specific (leaf class)
* method(StringBuilder sb)	✅ Yes (null can be assigned to StringBuilder)	Most specific (leaf class)
* method(CharSequence cs)	✅ Yes (null can be assigned to CharSequence)	Less specific (interface)

# The problem:
* Both String and StringBuilder are equally specific (both are leaf classes, neither extends the other).
* Java cannot decide between String and StringBuilder → ambiguous method call.
* CharSequence is less specific, so it's not chosen either.

# 🔑 Key Concepts to Remember:
* Rule	Explanation
* Most specific method	Java picks the most specific applicable method.
* Ambiguity	If two or more methods are equally specific, compilation fails.
* Sibling classes	String and StringBuilder are siblings → neither is more specific.
