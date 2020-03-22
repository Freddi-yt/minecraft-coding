### Create Command
``` java
package xyz.freddi.tutorial;

import org.bukkit.command.Command;
import org.bukkit.command.CommandExecutor;
import org.bukkit.command.CommandSender;
import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

	@Override
	public void onEnable() {
		...
		getCommand("tutorial").setExecutor(new CommandExecutor() {
			
			@Override
			public boolean onCommand(CommandSender sender, Command cmd, String label, String[] args) {
				
				
				return false;
			}
		});
	}

}
```

### Check if sender is a Player
``` java hl_lines="18 19 20 21 22 23 24 25"
package xyz.freddi.tutorial;

import org.bukkit.command.Command;
import org.bukkit.command.CommandExecutor;
import org.bukkit.command.CommandSender;
import org.bukkit.entity.Player;
import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

	@Override
	public void onEnable() {
		...
		getCommand("tutorial").setExecutor(new CommandExecutor() {

			@Override
			public boolean onCommand(CommandSender sender, Command cmd, String label, String[] args) {
				if (!(sender instanceof Player)) {
					sender.sendMessage("You are not a Player!");
					return true;
				}
				Player player = (Player) sender;
				player.sendMessage("Heyyy");

				return true;
			}
		});
	}

}
```

### Register Command in Plugin.yml
``` yml
name: Tutorial
author: Freddi
version: 1.0.0
main: xyz.freddi.tutorial.Tutorial
commands:
  tutorial:
```


