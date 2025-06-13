# Inheritance vs. Dependency
## Inheritance
```java
// 부모 클래스
class Animal {
    void speak() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

// 자식 클래스
class Dog extends Animal {
    @Override
    void speak() {
        System.out.println("멍멍!");
    }
}
```
## Dependency
```java
// 다른 클래스 (독립적)
class Printer {
    void print(String message) {
        System.out.println("출력: " + message);
    }
}

// 의존하는 클래스
class Report {
    void generate() {
        Printer printer = new Printer(); // Printer를 "잠깐 사용"
        printer.print("리포트 생성 완료");
    }
}
```