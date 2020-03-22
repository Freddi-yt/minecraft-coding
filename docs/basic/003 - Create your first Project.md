### Create
* Open Eclipse

* Click on "File" -> "New" -> "Java Project"

* Pick a Random Project name ("tutorial")

* Click on Finish

* Click on "Don´t Create" bc. we dont need a "module-info.java"

### Setup

* Right Click your Project and open the "Properties"

* Navigate to "Java Build Path" -> "Libraries" -> "Modulepath" and Click on "Add External JARs..."

* Select your spigot.jar

* Click on "Apply and Close"

* Right Click the "src" Package and go on "New" -> "Package"

* The name is made up of your domain and your project name. (Freddi.xyz -> "xyz.freddi.tutorial")

* And Click on Finish

* Right Click your created Package and create an new Class. ("New" -> "Class")

* The name is your Project name. ("Tutorial")

### Start Coding

* Now add "extends JavaPlugin" to your Main Class.

``` java hl_lines="3"
package xyz.freddi.tutorial;

public class Tutorial extends JavaPlugin {

}
```
 
* Import `import org.bukkit.plugin.java.JavaPlugin;`

!!! tip
    Press ++ctrl+shift+o++ to manage your Imports
``` java hl_lines="3"
package xyz.freddi.tutorial;

import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

}
```

* We start then easily and make a Hello World out put at the start.

``` java hl_lines="7 8 9 10"
package xyz.freddi.tutorial;

import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

	@Override
	public void onEnable() {
		System.out.println("Hello World");
	}

}

```



* Now you have to create the "plugin.yml" in the "src" Package. (Right click on "src" -> "New" -> "File" -> "plugin.yml")

* Open it in the "Text-Editor" inside of Eclipse.

``` yml
name: Tutorial
author: Freddi
version: 1.0.0
main: xyz.freddi.tutorial.Tutorial
```

### Build

* To Build just Right Click on your Project
* Click on "Export...".-> "Java" -> "JAR file" -> "Next >" -> all check boxes on the right
* Chose a export path
* Click on "Finish"