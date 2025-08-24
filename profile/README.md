## NexariaMC Info:
Nexaria is a public Minecraft server that features the gamemodes Lifesteam and MMORPG. The goal is to create a unique gameplay experience at a massive scale

## Developer Doc:
### Java/Kotlin Development Rules
* **Indentation:** Use 4 spaces for indentation.
* **Single Responsibility Principle:** Functions should adhere to the single concept principle. For example, a function named `loadPlayer` should only load player data and not perform other actions like setting blocks. Similarly, `updateSomething` should only perform the update. Generally ANY method/function MUST do only a specific concept.
* **API and Entrypoint Documentation:** The plugin's API and the main entrypoint (the class extending `JavaPlugin`) must have Javadoc comments explaining their purpose and usage.
