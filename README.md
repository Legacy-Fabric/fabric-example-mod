# Legacy Fabric Example Mod

- [Quick start guide](#quick-start-guide)
  - [Introduction to the folder structure](#introduction-to-the-folder-structure)
  - [Creating your mod](#creating-your-mod)
  - [Useful gradle commands](#useful-gradle-commands)
- [More info](#more-info)
- [License](#license)

## Quick start guide

### Introduction to the folder structure

**Build files:**

| File                | Description                                              |
| ------------------- | -------------------------------------------------------- |
| `build.gradle`      | Configures the compilation process.                      |
| `gradle.properties` | Contains properties for Minecraft, fabric, and your mod. |
| `settings.gradle`   | Configures the plugin repositories.                      |

**Fabric files:**

These files are located at `src/main/resources`.

| File                    | Description                              | Additional information                                                                                                |
| ----------------------- | ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `fabric.mod.json`       | Contains metadata about your mod.        | [wiki:fabric_mod_json_spec](https://fabricmc.net/wiki/documentation:fabric_mod_json_spec)                             |
| `modid.mixins.json`     | Contains a list of all your mixin files. | [wiki:mixin_registration](https://fabricmc.net/wiki/tutorial:mixin_registration)                                      |
| `assets/modid/icon.png` | The icon of your mod.                    | [wiki:fabric_mod_json_spec#icon](https://fabricmc.net/wiki/documentation:fabric_mod_json_spec?s[]=icon#custom_fields) |


### Creating your mod

First of you must replace all occurrences of `modid` with the id of your mod.

If your mod doesn't use mixins you can safely remove the mixin entry in your `fabric.mod.json` as well as delete any `*.mixin.json` files.

This template has the legacy fabric api included in it's build script, more info about the api can be found at it's [github repo](https://github.com/Legacy-Fabric/fabric).
If you know what you are doing you can also safely remove the api from the build script as it isn't required.

### Useful gradle commands

```sh
# Compile your mod
./gradlew build

# Remove old build files
./gradlew clean

# Generate Minecraft sources
./gradlew genSources

# Launch a modded Minecraft client
./gradlew runClient

# Kill gradle if it's doing stupid things
./gradlew --stop
```

## More info

Additional tutorials and tips can be found in the [wiki](https://github.com/Legacy-Fabric/fabric-example-mod/wiki).

For more detailed setup instructions please see the [fabric wiki](https://fabricmc.net/wiki/tutorial:setup).

If you are new to fabric or Minecraft modding in general then [this wiki page](https://fabricmc.net/wiki/tutorial:primer) may help you.

## License

This template is available under the CC0 license. Feel free to learn from it and incorporate it in your own projects.
