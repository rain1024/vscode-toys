# Getting Started with Kotlin in VSCode 🚀

Welcome to the Kotlin universe! Are you excited to craft some idiomatic, safe, and expressive code? Whether you're a seasoned Kotlin developer or new to this modern language, this guide is here to help you set up your VSCode environment for Kotlin development. Grab your favorite drink, and let's jump in!

## Step 1: Install the Kotlin Compiler (Kotlin SDK) 🧪

Before you can start writing Kotlin code, you'll need the Kotlin SDK, which serves as the foundation for your Kotlin projects.

If you're on macOS, you can use Homebrew to install the Kotlin compiler with the following command:

```
brew install kotlin
```

For other operating systems, visit the [Kotlin SDK download page](https://kotlinlang.org/docs/command-line.html) and follow the installation instructions.

## Step 2: Install Kotlin Extensions for VSCode 📦

VSCode extensions for Kotlin are like adding a drop of essence to your development experience. They supercharge your Kotlin development by providing features like code completion, linting, and more.

1. Open VSCode and navigate to the Extensions view by clicking the square icon on the sidebar or by pressing `Ctrl+Shift+X`.

2. In the Extensions search bar, install the following:

| Extension           | Publisher         | Description                                    |
|---------------------|-------------------|------------------------------------------------|
| Kotlin Language     | Mathias Fröhlich  | Kotlin language support, debugging, and more.  |
| Kotlin Test Explorer| Mathias Fröhlich  | Test Explorer for Kotlin, helpful for running JUnit tests.|

<table>
  <tr>
    <td><a href="">Code Runner</a></td>
    <td><a href="">Code Runner</a></td>
  </tr>
</table>

Your VSCode is now fully equipped for Kotlin development! 🎉

## Step 3: Create Your First Kotlin Project 🌟

Starting a Kotlin project in VSCode is simple and straightforward. Here's how to do it:

1. Open a new terminal in VSCode via `Terminal > New Terminal`.

2. Create a new directory and initialize your Kotlin project with:

```bash
mkdir myKotlinApp
cd myKotlinApp
touch Main.kt
```

3. Open `Main.kt` and write your first Kotlin program. Here's a simple "Hello, World!" example:

```kotlin
fun main() {
    println("Hello, World!")
}
```

4. To run your code, open the terminal and enter the following command:

```bash
kotlinc Main.kt -include-runtime -d Main.jar
java -jar Main.jar
```

Voilà! You just ran your first Kotlin program! 🥳

## Step 4: Write Tests with JUnit 4 🧪

JUnit 4 is one of the testing libraries that you can use to ensure your Kotlin code is working as expected. Here's a simple test for you.

First, add a `Tests.kt` file to your project and paste the following code:

```kotlin
import org.junit.Test
import org.junit.Assert.assertEquals

class Tests {

    @Test
    fun testHelloWorld() {
        assertEquals("Hello, World!", "Hello, World!")
    }
}
```

Then, add the JUnit 4 library to your classpath:

```bash
# Download junit.jar and hamcrest-core.jar from the official site
# Then add them to your classpath
kotlinc -cp junit-4.XX.YY.jar:hamcrest-core-1.XY.ZZ.jar -include-runtime -d Tests.jar Tests.kt
```

To run your test:

```bash
java -cp Tests.jar:junit-4.XX.YY.jar:hamcrest-core-1.XY.ZZ.jar org.junit.runner.JUnitCore Tests
```

Replace `XX.YY` and `1.XY.ZZ` with the versions you've downloaded.

## Additional Resources 📚

- [Kotlin documentation](https://kotlinlang.org/docs/home.html) - In-depth guides on Kotlin language features.
- [Debugging in Kotlin](https://kotlinlang.org/docs/debugging.html) - Debugging techniques specific to Kotlin.
- [Testing in Kotlin](https://kotlinlang.org/docs/testing.html) - Comprehensive guide on various testing frameworks supported in Kotlin.

## Wrapping Up 🎉

Congratulations, you've successfully set up your VSCode environment for Kotlin development. You're all set to create wonderful Kotlin applications. Happy coding! 🎈

---

*Ingredients used in this tutorial:*

- Kotlin 1.XX.XX
- macOS 13.2.1
- VSCode 1.81

---
