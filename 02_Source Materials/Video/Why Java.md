Tags: [[java_oop]] 

## Why we use Java

- Memiliki fitur OOP yang lengkap, sangat OOP banget.
- Compile sekali run dimana saja, jika bahasa C, kita tidak bisa copas hasil compile nya.
- Statically Typed → Ketika mendeklarasikan variable → `int x` , ada yang tidak statically typed contoh js → `let x`
- Battle Tested, sudah terjamin kualitasnya

## Java Installation

1. JDK (Java Development Kit) → Compile, debug, execute
2. JVM (Java Virtual Machine) → Byte code ke machine code
3. JRE (Java Runtime Engine) → Hampir sama dengan JVM, tapi ada java bin, dan class yang lain

## Alur dari Java

1. Source Code → `A.java`
2. JavaC (Java Compiler)
3. Byte Code → `A.class`
    1. Beda dengan C, kalau di C tidak ada byte code, dari Code langsung ke Native Machine Code
    2. Di java ada `.class`
4. JVM → Disini baru di translate ke Native Machine Code

## HelloWorld

- IDE: VSCode, Intellij IDea
```Java
public class Main{
	public static void main(String[] args){
		System.out.println("Hello World");
	}
}
```

- Cara Compile dan Run
```Powershell
javac Main.java
```

```Powershell
java Main --> ini JVM
```
