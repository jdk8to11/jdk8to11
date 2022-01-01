# jdk8to11

an easy way for your project codes compatible with jdk 8 and jdk 11+ 

## Terms of Use
No Warranty: THE SUBJECT SOFTWARE IS PROVIDED "AS IS" WITHOUT ANY WARRANTY OF ANY KIND, EITHER EXPRESSED, IMPLIED, OR STATUTORY, INCLUDING, BUT NOT LIMITED TO, ANY WARRANTY THAT THE SUBJECT SOFTWARE WILL CONFORM TO SPECIFICATIONS, ANY IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, OR FREEDOM FROM INFRINGEMENT, ANY WARRANTY THAT THE SUBJECT SOFTWARE WILL BE ERROR FREE, OR ANY WARRANTY THAT DOCUMENTATION, IF PROVIDED, WILL CONFORM TO THE SUBJECT SOFTWARE. THIS AGREEMENT DOES NOT, IN ANY MANNER, CONSTITUTE AN ENDORSEMENT BY GOVERNMENT AGENCY OR ANY PRIOR RECIPIENT OF ANY RESULTS, RESULTING DESIGNS, HARDWARE, SOFTWARE PRODUCTS OR ANY OTHER APPLICATIONS RESULTING FROM USE OF THE SUBJECT SOFTWARE. FURTHER, GOVERNMENT AGENCY DISCLAIMS ALL WARRANTIES AND LIABILITIES REGARDING THIRD-PARTY SOFTWARE, IF PRESENT IN THE ORIGINAL SOFTWARE, AND DISTRIBUTES IT "AS IS."

## how to use

+ upload all files in **lib** directory to your private maven repository.

+ add dependency for most situations

```
        <dependency>
            <groupId>jdk8to11</groupId>
            <artifactId>jdk8to11all</artifactId>
            <type>pom</type>
            <version>1.0</version>
        </dependency>
```

+ or add dependency, exclude sum.misc and javafx.util.Pair. 
```
        <dependency>
            <groupId>jdk8to11</groupId>
            <artifactId>jdk8to11</artifactId>
            <type>pom</type>
            <version>1.0</version>
        </dependency>
```

## what's the difference between jdk8to11 with jdk8to11all?
jdk8to11 only include dependencies from central maven repository,
jdk8to11all include all of jdk8to11 and extra libs,such as sum.misc and javafx.util.Pair.

## Where are the jars come form?
download from ```https://www.azul.com/downloads/?version=java-8-lts&package=jdk-fx```, trimed and striped.

## How to add support one binary jar for jdk11，which compiled from jdk8 ?
```
# download all dependencies to local target/dependency dir.
mvn -f jdk8to11-1.0.pom dependency:copy-dependencies

# add all needed dependencies  to the binary jar.
WINRAR :  功能添加-》文件-》不压缩直接存储的文件(压缩方式：存储)
jar:    jar -cfM0 new.jar * 
```


