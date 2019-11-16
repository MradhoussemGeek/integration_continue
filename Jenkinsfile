
pipeline {
    agent any

    stages {
        
        stage('build') {
        
            steps {
                bat label: '', script: 'mvn install '
            }
        }
        
        
        stage('checkout') {
            steps {
                git 'https://github.com/MradhoussemGeek/integration_continue'
            }
        }
        stage('Test') {
            steps {
                bat label: '', script: 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
             echo 'C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue>mvn deploy  
[INFO] Scanning for projects...
[INFO]                                                                         
[INFO] ------------------------------------------------------------------------
[INFO] Building Archetype - HelloWorld 0.0.1-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ maven-demo-1 ---
[WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue\\src\\main\\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ maven-demo-1 ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ maven-demo-1 ---
[WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue\\src\\test\\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ maven-demo-1 ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ maven-demo-1 ---
[INFO] No tests to run.
[INFO] 
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ maven-demo-1 ---
[WARNING] JAR will be empty - no content was marked for inclusion!
[INFO] 
[INFO] --- maven-install-plugin:2.4:install (default-install) @ maven-demo-1 ---
[INFO] Installing C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue\\target\\maven-demo-1-0.0.1-SNAPSHOT.jar to C:\\WINDOWS\\system32\\config\\systemprofile\\.m2\\repository\\tn\\esprit\\maven-demo-1\\0.0.1-SNAPSHOT\\maven-demo-1-0.0.1-SNAPSHOT.jar
[INFO] Installing C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue\\pom.xml to C:\\WINDOWS\\system32\\config\\systemprofile\\.m2\\repository\\tn\\esprit\\maven-demo-1\\0.0.1-SNAPSHOT\\maven-demo-1-0.0.1-SNAPSHOT.pom
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 2.099 s
[INFO] Finished at: 2019-11-16T11:02:50+01:00
[INFO] Final Memory: 10M/239M
[INFO] ------------------------------------------------------------------------
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (checkout)
[Pipeline] git
No credentials specified
 > git.exe rev-parse --is-inside-work-tree # timeout=10
Fetching changes from the remote Git repository
 > git.exe config remote.origin.url https://github.com/MradhoussemGeek/integration_continue # timeout=10
Fetching upstream changes from https://github.com/MradhoussemGeek/integration_continue
 > git.exe --version # timeout=10
 > git.exe fetch --tags --force --progress -- https://github.com/MradhoussemGeek/integration_continue +refs/heads/*:refs/remotes/origin/*
 > git.exe rev-parse "refs/remotes/origin/master^{commit}" # timeout=10
 > git.exe rev-parse "refs/remotes/origin/origin/master^{commit}" # timeout=10
Checking out Revision 088d86d85051c4b426245fb4e0da3cbe1036f249 (refs/remotes/origin/master)
 > git.exe config core.sparsecheckout # timeout=10
 > git.exe checkout -f 088d86d85051c4b426245fb4e0da3cbe1036f249
 > git.exe branch -a -v --no-abbrev # timeout=10
 > git.exe branch -D master # timeout=10
 > git.exe checkout -b master 088d86d85051c4b426245fb4e0da3cbe1036f249
Commit message: "jenkinsfile"
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Test)
[Pipeline] bat

C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue>mvn test 
[INFO] Scanning for projects...
[INFO]                                                                         
[INFO] ------------------------------------------------------------------------
[INFO] Building Archetype - HelloWorld 0.0.1-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ maven-demo-1 ---
[WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue\\src\\main\\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ maven-demo-1 ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ maven-demo-1 ---
[WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\\Program Files (x86)\\Jenkins\\workspace\\maven_continue\\src\\test\\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ maven-demo-1 ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ maven-demo-1 ---
[INFO] No tests to run.
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 1.799 s
[INFO] Finished at: 2019-11-16T11:02:59+01:00
[INFO] Final Memory: 8M/239M
[INFO] ------------------------------------------------------------------------'

            }}

        stage('mail') {
            steps {
             
             echo 'upload'
            }
        }
    }
}