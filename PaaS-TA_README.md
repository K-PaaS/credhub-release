## 01. Submodule modify : credhub (src/credhub)

> $ vi src/credhub/build.gradle
```diff
 buildscript {
         jsonPathVersion = '2.4.0'
         kotlinVersion = '1.3.72'
         ktlintVersion = '0.37.2'
-        mariadbJdbcVersion = '2.3.0'
+        mariadbJdbcVersion = '2.5.1'
         passayVersion = '1.6.0'
         postgresqlJdbcVersion = '42.2.14'
         spotBugsToolVersion = '3.1.9'

         springRestDocsVersion = '2.0.4.RELEASE'
         springSecurityOauth2Version = '2.5.0.RELEASE'
         springSecurityOauth2AutoconfigureVersion = '2.3.1.RELEASE'
+        log4jVersion = '2.17.0'
     }

```
<br/>

> $ vi src/credhub/applications/credhub-api/build.gradle
```diff
     implementation("org.apache.commons:commons-lang3:${apacheCommonsLang3Version}")
     implementation("commons-codec:commons-codec:${commonsCodecVersion}")

+    implementation("org.apache.logging.log4j:log4j-api:${log4jVersion}")
+    implementation("org.apache.logging.log4j:log4j-core:${log4jVersion}")
+    implementation("org.apache.logging.log4j:log4j-jul:${log4jVersion}")
+    implementation("org.apache.logging.log4j:log4j-slf4j-impl:${log4jVersion}")
+
     implementation('com.fasterxml.jackson.module:jackson-module-kotlin')
     implementation("org.jetbrains.kotlin:kotlin-stdlib-jdk8")
     implementation("org.jetbrains.kotlin:kotlin-reflect")

```

