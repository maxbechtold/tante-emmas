# Get Familiar
## 10 min

* start the launchscript
    * eclipse: TanteEmmas.launch
    * intellij: tante_emmas.xml -> .idea/runConfigurations
    * other: `java -cp [classpath] io.vertx.core.Launcher run net.amygdalum.tanteemmas.server.Server`
* browse to http://localhost:8080
* navigate through the application
* explore the source code

----

## Some Hints ...

* be sure that the previous server (Vert.x) was stopped before starting a server again (otherwise you might be testing on an old server)
* each recording run will replace existing recorded files. So if you want to keep old files, put them in a separate package before starting a new recording session
* read the javadocs for the used annotations. They will give you further hints you to accomplish succesful recordings
* do not rely on few tests, about 100 tests will produce an acceptable coverage  

---

# Install Testrecorder 
## 10 min

* put testrecorder-0.3.12-jar-with-dependencies.jar in your workspace
* add testrecorder-0.3.12-jar-with-dependencies.jar to your class path
* put `AgentConfig.java` (located in src/hints) in the package `net.amygdalum.tanteemmas.testrecorder` in your src/main/java folder 
* try to understand the configuration in `AgentConfig.java`

----

* modify the launch script by adding  `-javaagent:testrecorder-0.3.12-jar-with-dependencies.jar=net.amygdalum.tanteemmas.testrecorder.AgentConfig`
    * eclipse: run configurations -> TanteEmmas -> Arguments -> Vm Arguments
    * intellij: run -> edit configurations -> tante-emmas -> Vm Options
    * shell: 
    ```Bash
    java
      -cp [classpath]
      -javaagent:[...]
      io.vertx.core.Launcher run net.amygdalum.tanteemmas.server.Server
    ```

----

* start the launch script
    * if the message `loading AgentConfig` appears => everything ok
    * else if the message `loading default config` appears => agent has been loaded but configuration not found (maybe AgentConfig is not in the correct package or the run script references a different config)
    * else => agent has not been loaded => adjust the path to the testrecorder.jar
* stop the application
* annotate `PriceCalculator.computeFairPrice` with `@Recorded`

----

* start the launch script, the messages should be:
    * `loading AgentConfig`
    * `recording snapshots of ...`
* browse to http://localhost:8080
* navigate through the application
* watch the console for generated tests
* stop the server and examine the generated tests in the workspace target folder

----

* try out different customer names such as:
  * Michaela Mustermann
  * Otto Normalverbraucher
  * Armer Schlucker
  * Reicher Schnösel
  * Reicher Pinkel
  * Gerd Grosskunde
* Analyze the generated tests for the customers and see how testrecorder analysis tries to generate readable tests

----

* If you are finished
  * You may even add a customer in `CustomerRepo` to see how testrecorder generates tests for it
  * Feel free to add some new properties and explore how flexible testrecorder will adjust code generation
 