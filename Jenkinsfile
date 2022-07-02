@Library('jenkins-share-lib')
def gv

pipeline {
    agent none
    stages {
        stage("init") {
            agent {
                docker { image 'maven:3.8.1-adoptopenjdk-11' }
            }
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }
        // stage("build jar") {
        //     agent {
        //         docker { image 'maven:3.8.1-adoptopenjdk-11' }
        //     }
        //     steps {
        //         script {
        //             echo "building jar"
        //             // # s/d groovy file
        //             // gv.buildJar()
        //             // # s/d library
        //             buildJar()
        //         }
        //     }
        // }
        // stage("build image") {
        //     steps {
        //         script {
        //             echo "building image"
        //             // // # s/d groovy file
        //             // gv.buildImage()
        //             // # s/d library
        //             buildImage()
        //         }
        //     }
        // }
        stage("deploy") {
            agent {
                docker { image 'maven:3.8.1-adoptopenjdk-11' }
            }
            steps {
                script {
                    echo "deploying"
                    // gv.deployApp()
                    // # s/d library
                    deployApp "tienbm-test"
                }
            }
        }
    }   
}
