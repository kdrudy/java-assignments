## String Formatting

While it is okay to combine strings together using `+`, it can get ugly. For example, look at this gnarly line from yesterday's `ToDo` project:

```java
System.out.println(checkbox + i + ". " + item.text);
```

Even if you know what those variables contain, it can be hard to picture what will be printed. A simpler way to do this is string formatting. Fire up JREPL and try the following:

* `String name = "Alice";`
* `int age = 30;`
* `String.format("Hello, %s! You are %s years old.", name, age);`
* `System.out.printf("Hello, %s! You are %s years old.", name, age);`

Now let's rewrite that line in the `ToDo` project:

```java
System.out.printf("%s %s. %s\n", checkbox, i, item.text);
```

## Zoo

Create a project called `Zoo`. We'll use this to demonstracte a fundamental idea in Java called inheritance by extending animal classes. We'll start with a simple `Animal` class:

```java
public class Animal {
    String name;
}
```

Now make broad animal categories that inherit from it:

```java
public class Mammal extends Animal {
    public Mammal() {
        this.name = "Mammal";
    }
}
```

```java
public class Reptile extends Animal {
    public Reptile() {
        this.name = "Reptile";
    }
}
```

```java
public class Bird extends Animal {
    public Bird() {
        this.name = "Bird";
    }
}
```

Finally, make specific classes that inherit from those categories:

```java
public class Dog extends Mammal {
    public Dog() {
        this.name = "Dog";
    }
}
```

```java
public class Snake extends Reptile {
    public Snake() {
        this.name = "Snake";
    }
}
```

```java
public class Hawk extends Bird {
    public Hawk() {
        this.name = "Hawk";
    }
}
```