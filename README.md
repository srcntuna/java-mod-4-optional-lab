# Optional Lab

## Instruction

You are given the following code:

```java
import java.util.HashMap;
import java.util.Map;
import java.util.Optional;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String bookName = scanner.nextLine();
        Optional<String> optAuthor = Book.getAuthor(bookName);

        // write your code here
    }
}

// DO NOT MODIFY the code below //
class Book {
    private static final Map<String, String> books = new HashMap<>();

    static {
        books.put("Effective Java", "Joshua Bloch");
        books.put("Designing Data-Intensive Applications", "Martin Kleppmann");
        books.put("Modern Java in Action", "Raoul-Gabriel Urma");
    }

    static Optional<String> getAuthor(String name) {
        return Optional.ofNullable(books.get(name));
    }
}
```

Your task is to write code in the `main` method that will print the book name
along with its title if the book is present in the HashMap. Print the book’s
name and its author (separated by `written by`) if the author is present and the
“Unknown” string otherwise.

```plaintext
Example 1:

bookName = "Effective Java"

"Effective Java written by Joshua Bloch"
```

```plaintext
Example 2:

bookName = "BDD in Java"

"Unknown"
```
