
-  Scope where the dependencies will be used.
- **default** is `compile` time
- `compile` - `provided` - `runtime` - `test` - `system` - `import`

---

`compile`
This is the **default scope**, used if none is specified. Compile dependencies are available in all classpaths of a project. Use for libraries that your application needs to compile and run.

`provided`
Dependencies with `provided` scope are **required for compilation but are not included in the final packaging.** They are assumed to be provided by the runtime environment, such as a servlet container or an application server.

`runtime`
This scope indicates that the dependency is **not required for compilation, but is for execution**. Maven includes a dependency with this scope in the runtime and test classpaths, but not the compile classpath. Use for libraries that your application needs to run but not to compile.

`test`
This scope indicates that the dependency is not required for normal use of the application, and is only available for the test compilation and execution phases. Use for libraries that are needed only for testing purposes, such as JUnit or Mockito.

`system`
This scope is similar to provided except that you have to provide the JAR which contains it explicitly. The artifact is always available and is not looked up in a repository.

`import`
This scope is only supported on a dependency of type pom in the <dependencyManagement> section. It indicates the dependency is to be replaced with the effective list of dependencies in the specified POM's <dependencyManagement> section. Since they are replaced, dependencies with a scope of import do not actually participate in limiting the transitivity of a dependency.