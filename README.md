# Something about Java
@(示例笔记本)[Java]

#### 1. 面向对象的基本特征
- 抽象
- 封装
- 继承
- 多态

#### 2. String是基本数据类型吗？
不是。Java中的基本数据类型包括：byte,short,int,long,float,double,char,boolean。java.lang.String类是final类型的，因此不可以继承这个类，不能修改这个类。为了提高效率节省空间，我们应该用StringBuffer类。
#### 3. int和Integer有什么区别？
Java中提供了两种类型，基本类型和引用类型。int是Java中的基本数据类型，Integer是java为int提供的封装类。Java为每个基本类型提供了封装类。

| 基本数据类型      |     引用类型 |
| :-------- | :--------|
| byte    |  Byte  |
| short   |  Short |
| int     |  Integer | 
| long    |  Long  |
| float   |  Float |
| double  |  Double |
| char    |  Character  |
| boolean |  Boolean   |
基本类型和引用类型的行为完全不同，并且具有不同的语义。基本类型和引用类型具有不同的特征和用法，它们包括：大小和速度，这种类型以哪儿种类型的数据结构存储，当基本类型和引用类型当做某个类的实例数据时所指定的缺省值。对象引用实例变量的缺省值为null，而基本数据实例变量的缺省值和它们的类型有关。
#### 4. String和StringBuffer有什么区别？
Java平台提供了String和StringBuffer两个类来存储和操作字符串，即包含多个字符的字符数据。String类提供了字符不可改变的字符串。而StringBuffer提供的字符串可以进行修改。
#### 5. 运行时异常和一般异常有什么区别？
异常是指程序运行过程中出现的错误。Throwable是所有异常和错误的超类，有两个自类Error和Exceotion，分别表示错误和异常。而Exception又分为运行时异常和非运行时异常（一般异常）。Error是程序无法处理的错误，比如OutOfMemoryError等，这些错误发生时，JVM一般会选择终止线程。运行时异常，包括NullPointerException等，此类异常程序中不是必须捕获的。而非运行时异常，包括IOExceotion等，此类异常是程序中必须捕获的，否则编译都不通过。
#### 6. HashMap和HashTable的区别？
HashMap是Map接口的实现，非线程安全的，多线程访问的时候需要加同步锁，且允许空键值。
HashTable继承自Dictionary类，线程安全的，多线程访问时不需要加同步锁，不允许空键值。
HashMap和HashTable采用的hash/rehash算法都大概一样，所以性能不会有很大差异。