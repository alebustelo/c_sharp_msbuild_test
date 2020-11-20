//Declarative

pipeline {
  agent {
    label 'windows'
  }
  // tools {
  //     jdk 'java-11-openjdk'
  //     maven 'apache-maven-3.6.3'
  // }
  stages {
    stage('Clean Workspace before run') {
      steps {
        bat 'del *.* /F /Q'
      }
    }
    stage('Checkout code') {
      steps {
        checkout scm
      }
    }
    stage('Build C# code') {
      steps {
        // bat 'csc helloworld.cs'
        bat 'msbuild helloworld.csproj -p:AssemblyName=Greetings'
      }
    }
    stage('Run C# code') {
      steps {
        bat "Bin\\Greetings.exe"
      }
    }
    stage('Clean Workspace after run') {
      steps {
        bat 'del *.* /F /Q'
      }
    }
  }
}
