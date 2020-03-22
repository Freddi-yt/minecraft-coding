### Create Command
``` java
package xyz.freddi.tutorial;

import java.util.List;

import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.command.TabCompleter;
import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

	@Override
	public void onEnable() {
		...
		getCommand("tutorial").setTabCompleter(new TabCompleter() {
			
			@Override
			public List<String> onTabComplete(CommandSender sender, Command cmd, String label, String[] args) {
				return null;
			}
			
		});
	}

}

```

### with feedback
``` java hl_lines="20"
package xyz.freddi.tutorial;

import java.util.Arrays;
import java.util.List;

import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.command.TabCompleter;
import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

	@Override
	public void onEnable() {
		...
		getCommand("tutorial").setTabCompleter(new TabCompleter() {
			
			@Override
			public List<String> onTabComplete(CommandSender sender, Command cmd, String label, String[] args) {
				return Arrays.asList("foo", "bar");
			}

		});
	}

}
```

