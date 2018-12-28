# 注解
### 注解是Java SE5引入的, Java SE5其内置准注解包括:

@Override - 表示当前的方法定义将覆盖超类中的方法

@Deprecated - 表示方法已过时

@SuppressWarnings - 关闭不当的编译器警告信息

### 基本语法
```java
  @Target(ElementType.METHOD)
  @Retention(RetentionPolicy.RUNTIME)
  public @interface Test{}
```

标记注解marker-annotation: 没有元素的注解,如@Test就是一个标记注解

元注解meta-annotation:  

@Target - 表示该注解可以用于什么地方,其可能的ElementType参数包括

- CONSTRUCTOR 构造器的声明
- FIELD 域声明
- LOCAL_VARIABLE 局部变量声明
- MEHTOD 方法声明
- PACKAGE 包声明
- PARAMETER 参数声明
- TYPE 类,接口或enum声明

@Retention - 表示需要什么级别保存该注解信息,其可能的RetentionPolicy参数包括

- SOURCE 注解将被编译器丢弃
- CLASS 注解在class文件中可用,将会被VM丢弃
- RUNTIME VM将在运行期也保留注解,因此可以通过反射信息读取注解的信息

@Documented - 将此注解包含在JavaDoc中

@Inherited - 允许子类集成父类中的注解


