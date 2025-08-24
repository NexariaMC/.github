## NexariaMC Info:
Nexaria is a public Minecraft server that features the gamemodes Lifesteam and MMORPG. The goal is to create a unique gameplay experience at a massive scale

## Developer Doc:
### Java/Kotlin Development Rules
* **Sanitization** ALWAYS assume something does not exist in the current scope of your load. For example, check if a config file exists and is valid before loading it. We want more errors as values or logging than exceptions.
* **Errors as values** If a function can throw an error but can be replaced with an object that represents a return, it should do that, if its a `void` function and it throws a `RuntimeException` in a check, it should be returning a boolean. If an exception MUST be thrown, make sure the message is clear and understanable and documented.
* **Privatization** If a function is intended exclusively to be ran by the developer in specific cases but cannot be private or package private, it must be annotated by `@ApiStatus.Internal`.
* **Null Safety** Functions are responsible for accounting for null safety, if a parameter or a class field CAN be null it must be annotated by `@Nullable`. Anything not annotated `@Nullable` will be assumed to be not null at all times.
* **Indentation:** Use 4 spaces for indentation.
* **Single Responsibility Principle:** Functions should adhere to the single concept principle. For example, a function named `loadPlayer` should only load player data and not perform other actions like setting blocks. Similarly, `updateSomething` should only perform the update. Generally ANY method/function MUST do only a specific concept.
* **API and Entrypoint Documentation:** The plugin's API and the main entrypoint (the class extending `JavaPlugin`) must have Javadoc comments explaining their purpose and usage.
