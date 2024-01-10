# Kafka Node Simulator

## Overview
This project is a Kafka Node Simulator that utilizes Protocol Buffers (protobuf) for message serialization. It includes a `event.proto` file, which is used to generate Java classes representing events.

## Prerequisites
- Java JDK 17
- Maven 3.x
- Ensure that the JAVA_HOME environment variable is set to the JDK installation directory

## Compiling the Project
1. **Clone the Repository**: First, clone this repository to your local machine using Git.

    ```bash
    git clone https://github.com/mhafidi/kakfa-node-simulator.git
    ```

2. **Navigate to the Project Directory**: Change into the project directory.

    ```bash
    cd kakfa-node-simulator
    ```

3. **Compile Protocol Buffers File**: The `event.proto` file needs to be compiled to generate Java classes. This is handled automatically by the Maven build process.

   The protobuf Maven plugin defined in `pom.xml` is configured to recognize `.proto` files in the `src/main/proto` directory. Ensure your `event.proto` file is located there.

4. **Build the Project**: Use Maven to compile the project and generate the required Java classes from the `.proto` file.

    ```bash
    mvn clean compile
    ```

   This command cleans the `target` directory (if it exists), and then compiles the source code. The protobuf Maven plugin will compile `event.proto` and generate Java classes in the `target/generated-sources` directory.

5. **Package the Application**: (Optional) If you want to package the application into a JAR, use:

    ```bash
    mvn package
    ```

   This will create a JAR file in the `target` directory.

## Using the Generated Java Classes
After compilation, the generated Java classes will be in the `target/generated-sources/protobuf/java/` directory. You can use these classes in your application to interact with event messages as defined in the `event.proto`.

For more detailed information about working with Protocol Buffers and Maven, refer to the [Protocol Buffers Documentation](https://developers.google.com/protocol-buffers) and the [Maven Documentation](https://maven.apache.org/guides/index.html).

## Troubleshooting
- If you encounter any issues with the `mvn compile` step, ensure that Maven is correctly installed and your JAVA_HOME is set.
- For problems related to Protocol Buffers compilation, verify the version compatibility of protobuf-java and protoc in `pom.xml`.

---

This README assumes a basic familiarity with Maven, Java, and Protocol Buffers. If you are new to any of these, it's recommended to familiarize yourself with their basics to effectively work with this project.
