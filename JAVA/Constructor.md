# 생성자 Constructor

> special method that is called when an object is instantiated (created)

## Idea
* 우리는 다양한 Object를 가지고 싶다.

```java
public class Human {
    // same name with class
    // setup 3 attributes. and these are the rues.
    String name;
    int age;
    double wight;

    Human(String name, int age, double weight) {
        
    }
}
```

When we want create a new Human, there are rules.
Human has 3 attributes.

``` java
Human human = new Human("Rick",65,70);
```

Now we can make the second human.

``` java
public class Human {
    // same name with class
    // setup 3 attributes. and these are the rues.
    String name;
    int age;
    double wight;
    
    Human(String name, int age, double weight) {
        this.name = name;
        this.age = age;
        this.weight = weight;
        
    }
}
```

`this` means `object`



