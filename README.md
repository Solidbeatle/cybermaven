# Cyber Maven Project

Welcome to the **Cyber** Maven project! This repository contains the source code for creating a Minecraft plugin using Maven, tailored for both PaperMC and SpigotMC. Follow this guide to set up and start your project with ease.

---

## 🌟 Features

- **Maven Build System**: Simplifies dependency management and project builds.
- **Cross-Compatible**: Works with both PaperMC and SpigotMC APIs.
- **Developer-Friendly**: Includes example configurations and clear documentation.

---

## 🛠️ Requirements

- **Java Version**: Java 17 or higher
- **Build Tool**: Maven 3.6 or higher
- **Minecraft Server Software**: PaperMC or SpigotMC

---

## 🚀 Getting Started

### Cloning the Repository

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/Solidbeatle/cybermaven.git
   ```
2. Navigate to the project directory:
   ```bash
   cd cyber
   ```

### Setting Up the Project

1. Ensure Java and Maven are installed on your system.
   - Verify Java version:
     ```bash
     java -version
     ```
   - Verify Maven version:
     ```bash
     mvn -v
     ```

2. Open the `pom.xml` file and configure the `groupId`, `artifactId`, and `version` as per your plugin’s details:
   ```xml
   <groupId>com.example.cyber</groupId>
   <artifactId>cyber-plugin</artifactId>
   <version>1.0.0</version>
   ```

### Example `pom.xml` for PaperMC and SpigotMC

Here is a sample `pom.xml` file configured for both PaperMC and SpigotMC:

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example.cyber</groupId>
    <artifactId>cyber-plugin</artifactId>
    <version>1.0.0</version>
    <name>Cyber Plugin</name>
    <description>A Minecraft plugin built with Maven for PaperMC and SpigotMC.</description>

    <dependencies>
        <!-- PaperMC API -->
        <dependency>
            <groupId>io.papermc.paper</groupId>
            <artifactId>paper-api</artifactId>
            <version>1.20.1-R0.1-SNAPSHOT</version>
            <scope>provided</scope>
        </dependency>

        <!-- SpigotMC API -->
        <dependency>
            <groupId>org.spigotmc</groupId>
            <artifactId>spigot-api</artifactId>
            <version>1.20.1-R0.1-SNAPSHOT</version>
            <scope>provided</scope>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <source>17</source>
                    <target>17</target>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>
```

---

## 🧱 Project Structure

- **`src/main/java`**: Core source code.
- **`src/main/resources`**: Plugin resources (e.g., `plugin.yml`).
- **`pom.xml`**: Maven configuration file for dependencies and builds.

### Example `plugin.yml`

Ensure the `plugin.yml` file is in the `src/main/resources` directory:
```yaml
name: Cyber
main: com.example.cyber.Main
version: 1.0.0
description: A Minecraft plugin example.
author: YourName
api-version: 1.20
```

---

## 🔨 Building the Plugin

Run the following command to build the plugin:
```bash
mvn clean package
```
The compiled JAR file will be in the `target` directory.

### Deploying to Minecraft Server

1. Copy the generated JAR file from the `target` directory to your server's `plugins` folder.
2. Restart your Minecraft server.
3. Check the server console to ensure the plugin loads correctly.

---

## 🤝 Contributing

We welcome contributions to improve this template! Here's how you can get involved:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add feature: your-feature-description"
   ```
4. Push the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute the code as outlined in the license.

---

## 📧 Support

For questions or support, feel free to reach out:

- **GitHub Issues**: [Submit an issue] (https://github.com/Solidbeatle/cybermaven/issues)
- **Email**: support@cyber.com

Thank you for using the Cyber Maven project. Happy coding! 🎮
