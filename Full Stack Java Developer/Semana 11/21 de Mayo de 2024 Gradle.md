![[Pasted image 20240521162722.png]]


https://gradle.org/
![[Pasted image 20240521113606.png]]

https://gradle.org/releases/?_gl=1*1sgxbed*_ga*MTMwNDM1MDI1MS4xNzE2MzEyOTA3*_ga_7W7NC6YNPT*MTcxNjMxMjkwNy4xLjEuMTcxNjMxMjkxOC40OS4wLjA.
![[Pasted image 20240521113622.png]]
![[Pasted image 20240521114911.png]]
![[Pasted image 20240521114919.png]]
# Gradle

Gestionar dependencias

Crear nuestro proyecto en Spring Boot

---
![[Pasted image 20240521121141.png]]

![[Pasted image 20240521121452.png]]
![[Pasted image 20240521122428.png]]
![[Pasted image 20240521122459.png]]
![[Pasted image 20240521122511.png]]
![[Pasted image 20240521122534.png]]
![[Pasted image 20240521122606.png]]
![[Pasted image 20240521122617.png]]
![[Pasted image 20240521122810.png]]
![[Pasted image 20240521122842.png]]
![[Pasted image 20240521122900.png]]

```sh
C:\Windows\System32🔒 [🦀 ]
❯ gradle -v

Welcome to Gradle 8.7!

Here are the highlights of this release:
 - Compiling and testing with Java 22
 - Cacheable Groovy script compilation
 - New methods in lazy collection properties

For more details see https://docs.gradle.org/8.7/release-notes.html


------------------------------------------------------------
Gradle 8.7
------------------------------------------------------------

Build time:   2024-03-22 15:52:46 UTC
Revision:     650af14d7653aa949fce5e886e685efc9cf97c10

Kotlin:       1.9.22
Groovy:       3.0.17
Ant:          Apache Ant(TM) version 1.10.13 compiled on January 4 2023
JVM:          17.0.11 (Oracle Corporation 17.0.11+7-LTS-207)
OS:           Windows 11 10.0 amd64


C:\Windows\System32🔒 [🦀 ]
❯ cd "C:\Users\Erick\Documents\CH-39"

~\Documents\CH-39
❯ cd "C:\Users\Erick\Documents\CH-39\GradleProject"

Documents\CH-39\GradleProject
❯ ls

Documents\CH-39\GradleProject
❯ gradle init
Starting a Gradle Daemon (subsequent builds will be faster)

Select type of build to generate:
  1: Application
  2: Library
  3: Gradle plugin
  4: Basic (build structure only)
Enter selection (default: Application) [1..4] 1

Select implementation language:
  1: Java
  2: Kotlin
  3: Groovy
  4: Scala
  5: C++
  6: Swift
Enter selection (default: Java) [1..6] 1

Enter target Java version (min: 7, default: 21): 17

Project name (default: GradleProject):

Select application structure:
  1: Single application project
  2: Application and library project
Enter selection (default: Single application project) [1..2] 1

Select build script DSL:
  1: Kotlin
  2: Groovy
Enter selection (default: Kotlin) [1..2] 2

Select test framework:
  1: JUnit 4
  2: TestNG
  3: Spock
  4: JUnit Jupiter
Enter selection (default: JUnit Jupiter) [1..4] 4

Generate build using new APIs and behavior (some features may change in the next minor release)? (default: no) [yes, no] no


> Task :init
To learn more about Gradle by exploring our Samples at https://docs.gradle.org/8.7/samples/sample_building_java_applications.html

BUILD SUCCESSFUL in 14m 39s
1 actionable task: 1 executed

Documents\CH-39\GradleProject [🅶 v8.7][☕ v17.0.11][⏱ 14m40s]
❯
```


---
![[Pasted image 20240521123143.png]]

```sh
Documents\CH-39\GradleProject [🅶 v8.7][☕ v17.0.11][⏱ 14m40s]
❯ gradle run

> Task :app:run
Hello World!

BUILD SUCCESSFUL in 7s
2 actionable tasks: 2 executed

Documents\CH-39\GradleProject [🅶 v8.7][☕ v17.0.11][⏱ 7s]
❯
```

---
![[Pasted image 20240521124302.png]]

---
Como inicializar projectos sin tanta configuracion 

![[Pasted image 20240521132948.png]]

https://start.spring.io/


![[Pasted image 20240521133153.png]]

![[Pasted image 20240521133347.png]]
![[Pasted image 20240521133423.png]]
![[Pasted image 20240521133517.png]]
![[Pasted image 20240521133608.png]]
![[Pasted image 20240521133707.png]]
![[Pasted image 20240521133740.png]]
![[Pasted image 20240521134307.png]]
![[Pasted image 20240521134536.png]]
Los añadimos a nuestro workspace de eclipse

![[Pasted image 20240521135850.png]]
![[Pasted image 20240521135936.png]]
![[Pasted image 20240521140735.png]]
![[Pasted image 20240521140854.png]]

# Añadiendo dependencias extras

![[Pasted image 20240521141020.png]]
![[Pasted image 20240521141108.png]]
![[Pasted image 20240521141151.png]]
![[Pasted image 20240521141138.png]]
![[Pasted image 20240521141209.png]]


---
![[Pasted image 20240521141511.png]]
![[Pasted image 20240521141638.png]]

---
![[Pasted image 20240521153543.png]]
![[Pasted image 20240521153853.png]]
![[Pasted image 20240521154429.png]]
![[Pasted image 20240521154734.png]]



---
![[Pasted image 20240521155012.png]]

![[Pasted image 20240521155031.png]]
![[Pasted image 20240521155024.png]]
![[Pasted image 20240521155044.png]]
![[Pasted image 20240521155140.png]]

```sh
. ____ _ __ _ _

/\\ / ___'_ __ _ _(_)_ __ __ _ \ \ \ \

( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \

\\/ ___)| |_)| | | | | || (_| | ) ) ) )

' |____| .__|_| |_|_| |_\__, | / / / /

=========|_|==============|___/=/_/_/_/

:: Spring Boot :: (v3.2.5)

  

2024-05-21T15:49:18.193-06:00 INFO 44892 --- [userProfile] [ main] o.g.userProfile.UserProfileApplication : Starting UserProfileApplication using Java 17.0.11 with PID 44892 (C:\Users\Erick\eclipse-workspace\userProfile\bin\main started by Erick in C:\Users\Erick\eclipse-workspace\userProfile)

2024-05-21T15:49:18.200-06:00 INFO 44892 --- [userProfile] [ main] o.g.userProfile.UserProfileApplication : No active profile set, falling back to 1 default profile: "default"

2024-05-21T15:49:19.229-06:00 INFO 44892 --- [userProfile] [ main] o.s.b.w.embedded.tomcat.TomcatWebServer : Tomcat initialized with port 8080 (http)

2024-05-21T15:49:19.243-06:00 INFO 44892 --- [userProfile] [ main] o.apache.catalina.core.StandardService : Starting service [Tomcat]

2024-05-21T15:49:19.243-06:00 INFO 44892 --- [userProfile] [ main] o.apache.catalina.core.StandardEngine : Starting Servlet engine: [Apache Tomcat/10.1.20]

2024-05-21T15:49:19.303-06:00 INFO 44892 --- [userProfile] [ main] o.a.c.c.C.[Tomcat].[localhost].[/] : Initializing Spring embedded WebApplicationContext

2024-05-21T15:49:19.305-06:00 INFO 44892 --- [userProfile] [ main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 1054 ms

2024-05-21T15:49:19.682-06:00 INFO 44892 --- [userProfile] [ main] o.s.b.w.embedded.tomcat.TomcatWebServer : Tomcat started on port 8080 (http) with context path ''

2024-05-21T15:49:19.692-06:00 INFO 44892 --- [userProfile] [ main] o.g.userProfile.UserProfileApplication : Started UserProfileApplication in 1.881 seconds (process running for 2.227)

2024-05-21T15:49:33.522-06:00 INFO 44892 --- [userProfile] [nio-8080-exec-1] o.a.c.c.C.[Tomcat].[localhost].[/] : Initializing Spring DispatcherServlet 'dispatcherServlet'

2024-05-21T15:49:33.522-06:00 INFO 44892 --- [userProfile] [nio-8080-exec-1] o.s.web.servlet.DispatcherServlet : Initializing Servlet 'dispatcherServlet'

2024-05-21T15:49:33.523-06:00 INFO 44892 --- [userProfile] [nio-8080-exec-1] o.s.web.servlet.DispatcherServlet : Completed initialization in 1 ms
```


---
https://spring.io/quickstart
![[Pasted image 20240521161111.png]]
![[Pasted image 20240521161142.png]]
![[Pasted image 20240521161308.png]]
![[Pasted image 20240521162031.png]]
![[Pasted image 20240521162219.png]]
![[Pasted image 20240521162513.png]]
