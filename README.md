# ANSI Escape Sequences

In programming and text formatting, escape sequences are special character combinations used to represent actions or formatting options. They are commonly used to add colors, formatting, and other visual effects to text in console or terminal outputs.

Escape sequences are represented by a backslash followed by specific characters. These sequences modify the appearance of the text when used in combination with a compatible terminal or console.

## Colors and Formatting

| **Formatting Option** | Escape Sequence | **Color** | Text Color (Dark) | Text Color (Bright) |
| :-------------------: | :-------------: | :-------: | :---------------: | :-----------------: |
|         Bold          |     \033[1m     |   Black   |     \033[30m      |      \033[90m       |
|          Dim          |     \033[2m     |    Red    |     \033[31m      |      \033[91m       |
|       Underline       |     \033[4m     |   Green   |     \033[32m      |      \033[92m       |
|         Blink         |     \033[5m     |  Yellow   |     \033[33m      |      \033[93m       |
|        Reverse        |     \033[7m     |   Blue    |     \033[34m      |      \033[94m       |
|        Hidden         |     \033[8m     |  Magenta  |     \033[35m      |      \033[95m       |
|                       |                 |   Cyan    |     \033[36m      |      \033[96m       |
|                       |                 |   White   |     \033[37m      |      \033[97m       |

## Using Escape Sequences in Programming Languages

Here are examples of how to use escape sequences for colors in some popular programming languages:

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "\033[31m"; // Set text color to red
    cout << "This is red text";
    cout << "\033[0m"; // Reset text color to default

    return 0;
}
```

### Python

```python
print("\033[31m" + "This is red text" + "\033[0m")
```

### Java

```java
public class Main {
    public static void main(String[] args) {
        System.out.print("\033[31m"); // Set text color to red
        System.out.print("This is red text");
        System.out.print("\033[0m"); // Reset text color to default
    }
}
```

### JavaScript(Node.js)

```javascript
console.log("\u001b[31m" + "This is red text" + "\u001b[0m");
```

### Ruby

```ruby
puts "\e[31mThis is red text\e[0m"
```

### Go

```go
package main

import "fmt"

func main() {
    fmt.Print("\033[31m") // Set text color to red
    fmt.Print("This is red text")
    fmt.Print("\033[0m") // Reset text color to default
}
```

## Additional Notes

- Escape sequences are based on the ANSI escape codes, which are a standardized set of sequences used for formatting text in terminals and consoles. These codes provide a consistent way to apply colors and other formatting options across different platforms and terminals.

- Standard escape codes can have different representations:

  - Decimal: The decimal representation of the escape code is 27.
  - Octal: The octal representation of the escape code is \033 or \o33, where 33 is the octal code.
  - Hexadecimal: The hexadecimal representation of the escape code is \x1B or \x1b, where 1B is the hexadecimal code.
  - C-escape: The C-escape representation of the escape code is \e or \E.
  - Ctrl-Key: The Ctrl-Key representation of the escape code is ^[, where ^ represents the Ctrl key and [ is the literal opening square bracket.

- Escape sequences can be followed by a command, sometimes delimited by an opening square bracket `[`. This is known as a Control Sequence Introducer (CSI). The CSI can be followed by arguments, separated by semicolons (`;`), and the command itself.

- Escape sequences can include the "?" character as part of the command. The "?" is used to introduce private or non-standard commands that are specific to certain terminals or consoles.

- It's important to note that not all escape sequences and commands are universally supported across all terminals or consoles. Some terminals may have limited support or may interpret certain commands differently. It's recommended to refer to the documentation or specifications of the specific terminal or console you're working with to ensure compatibility and desired behavior.

- When using escape sequences, it's important to consider the readability and accessibility of your text. While colors and formatting can enhance the visual appearance, certain combinations or excessive use of effects may hinder readability, especially for visually impaired users. It's advisable to choose color combinations and formatting options that ensure clear legibility and appropriate contrast.

- Escape sequences are not limited to just colors. They can also be used to apply other formatting options such as bold text, underlined text, or blinking text. The specific escape sequences for these formatting options may vary depending on the terminal or console being used.

- Some programming languages or frameworks provide higher-level abstractions or libraries for working with escape sequences and applying colors or formatting. These abstractions often simplify the usage and provide convenient functions or methods for applying colors and formatting to text output. It's recommended to check the documentation of your specific programming language or framework to see if such abstractions are available.
