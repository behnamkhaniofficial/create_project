# create_project
 یک پوشه پروژه ایجاد کنید Gradle وظیفه ای داخلی به نام همراه initدارد که پروژه Gradle جدید را در یک پوشه خالی شروع می کند. این initکار wrapperبرای ایجاد یک اسکریپت Gradle wrapper از کار (همچنین داخلی) استفاده می کند gradlew.  اولین قدم ایجاد پوشه ای برای پروژه جدید و تغییر فهرست در آن است.  $ mkdir نسخه ی نمایشی $ cd demo وظیفه init را اجرا کنید از داخل پوشه پروژه جدید، اجرای initکار با استفاده از دستور زیر را در ترمینال: gradle init. وقتی از شما خواسته شد ، 2: applicationنوع پروژه را 3: Javaبه عنوان زبان اجرا انتخاب کنید. سپس ، را انتخاب کنید 2: Add library projects. در مرحله بعدی می توانید DSL را برای نوشتن متن های ساختاری - 1 : Groovyیا انتخاب کنید 2: Kotlin. برای س questionsالات دیگر ، Enter را فشار دهید تا از مقادیر پیش فرض استفاده شود.  خروجی به این شکل خواهد بود:
 
e output will look like this:

$ gradle init

Select type of project to generate:
  1: basic
  2: application
  3: library
  4: Gradle plugin
Enter selection (default: basic) [1..4] 2

Split functionality across multiple subprojects?:
   1: no - only one application project
   2: yes - application and library projects
Enter selection (default: no - only one application project) [1..2] 2

Select implementation language:
  1: C++
  2: Groovy
  3: Java
  4: Kotlin
  5: Scala
  6: Swift
Enter selection (default: Java) [1..6] 3

Select build script DSL:
  1: Groovy
  2: Kotlin
Enter selection (default: Groovy) [1..2] 1

Select test framework:
  1: JUnit 4
  2: TestNG
  3: Spock
  4: JUnit Jupiter
Enter selection (default: JUnit 4) [1..4]

Project name (default: demo):
Source package (default: demo):

The init task generates the new project with the following structure:

Groovy
├── gradle 
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew 
├── gradlew.bat 
├── settings.gradle 
├── buildSrc
│   ├── build.gradle 
│   └── src
│       └── main
│           └── groovy 
│               ├── demo.java-application-conventions.gradle
│               ├── demo.java-common-conventions.gradle
│               └── demo.java-library-conventions.gradle
├── app
│   ├── build.gradle 
│   └── src
│       ├── main 
│       │   └── java
│       │       └── demo
│       │           └── app
│       │               ├── App.java
│       │               └── MessageUtils.java
│       └── test 
│           └── java
│               └── demo
│                   └── app
│                       └── MessageUtilsTest.java
├── list
│   ├── build.gradle 
│   └── src
│       ├── main 
│       │   └── java
│       │       └── demo
│       │           └── list
│       │               └── LinkedList.java
│       └── test 
│           └── java
│               └── demo
│                   └── list
│                       └── LinkedListTest.java
└── utilities
    ├── build.gradle 
    └── src
        └── main 
            └── java
                └── demo
                    └── utilities
                        ├── JoinUtils.java
                        ├── SplitUtils.java
                        └── StringUtils.java

Kotlin
├── gradle 
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew 
├── gradlew.bat 
├── settings.gradle.kts 
├── buildSrc
│   ├── build.gradle.kts 
│   └── src
│       └── main
│           └── kotlin 
│               ├── demo.java-application-conventions.gradle.kts
│               ├── demo.java-common-conventions.gradle.kts
│               └── demo.java-library-conventions.gradle.kts
├── app
│   ├── build.gradle.kts 
│   └── src
│       ├── main 
│       │   └── java
│       │       └── demo
│       │           └── app
│       │               ├── App.java
│       │               └── MessageUtils.java
│       └── test 
│           └── java
│               └── demo
│                   └── app
│                       └── MessageUtilsTest.java
├── list
│   ├── build.gradle.kts 
│   └── src
│       ├── main 
│       │   └── java
│       │       └── demo
│       │           └── list
│       │               └── LinkedList.java
│       └── test 
│           └── java
│               └── demo
│                   └── list
│                       └── LinkedListTest.java
└── utilities
    ├── build.gradle.kts 
    └── src
        └── main 
            └── java
                └── demo
                    └── utilities
                        ├── JoinUtils.java
                        ├── SplitUtils.java
                        └── StringUtils.java
