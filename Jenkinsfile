@Library('jenkins-share-lib')
def gv

pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }
        stage("build jar") {
            steps {
                script {
                    echo "building jar"
                    // # s/d groovy file
                    // gv.buildJar()
                    // # s/d library
                    buildJar()
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    echo "building image"
                    // // # s/d groovy file
                    // gv.buildImage()
                    // # s/d library
                    buildImage()
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    echo "deploying"
                    // gv.deployApp()
                    // # s/d library
                    deployApp()
                }
            }
        }
    }   
}