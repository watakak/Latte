# Latte | The new Programming Language

Many dream of venturing into Java development, only to feel lost and intimidated when they begin learning the language. Questions like "How do I create a project?" or "What are classes?" can be overwhelming. The complexities of compiling, the differences between Maven and Gradle, and the overarching question of how to learn it all contribute to discouraging beginners from pursuing further study. Java's intricate syntax, numerous unfamiliar buttons, and other challenges often drive newcomers away. In contrast, languages like Python are praised for their speed, simplicity, and intuitive syntax, making them easier to learn.

However, Python falls short in replicating many aspects of Java's functionality, especially when it comes to tasks like developing a plugin for Minecraft and compiling it into a .jar format—something Python physically cannot achieve.

**Introducing Latte: The Solution**

Latte is a hybrid programming language based on Python, designed to make Java project development accessible. It combines the ease of creating Java projects with a lightweight syntax, an intuitive interface, and a focus on user-friendly language interactions. Latte aims to eliminate the steep learning curve associated with Java. Even without tutorials, beginners can effortlessly create projects, a feat often challenging in Java. Latte is currently tailored for writing Minecraft plugins, serving as its primary objective. Nevertheless, it is versatile enough to create standard Java projects with ease. In essence, Latte is a brilliant concept that I am eager to bring to life through my efforts!

### Quick Tutorial:

1. Launch IntCode (the Latte IDE).
2. Click "New Project" and then "New Latte Project" to create a project.
3. In the project creation window, choose "Minecraft Plugin."
4. Input necessary data, for example:
   - Project Name: "HelloPlayer"
   - Author: "watakak"
   - Version of Plugin: 1.0
   - Description: "Greets players upon joining the server and includes two commands."
5. You're all set! Your project structure will look like this:
   - LatteProjects
     - HelloPlayer
       - HelloPlayer.latte
       - plugin.yml
6. Let's start coding! Here's a sample Latte code:

```latte
nickname = player.name

on starting():
    console.print('Plugin enabled!')

on working():
    on player.join():
        player.print('Welcome to the server, {nickname}!')
    if player type '/hello':
        player.print('Hello!')
    elif player type '/hello all' -p 'HelloPlayer.helloall':
        server.print('Hello, everyone!')

on stopping():
    server.print('Server is going to stop in the next 3 seconds!')
    wait(3)
    console.print('Plugin disabled.')
```

7. Click "Build" in the IDE. Later, find the .jar file along the path:
   - LatteProjects
     - HelloPlayer
       - Builds
         - HelloPlayer-1.0.jar
       - HelloPlayer.latte
       - plugin.yml
8. That's it! You can now transfer the .jar file to your Minecraft server and run it. You've learned how to write plugins for your Minecraft server using Latte!

In conclusion, Latte is a relatively new, convenient, and lightweight language that simplifies code writing, making it intuitive for programming beginners. With Latte, newcomers can develop an interest in both Python and Java programming, bringing their projects to life. 
