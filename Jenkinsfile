pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP-REPO = 'vprofile-snapshot'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'sanju'
        RELEASE-REPO = 'vprofile-release'
        CENTRAL-REPO = 'vpro-maven-central'
        NEXUS-GRP-REPO = 'vprofile-maven-group'
        NEXUSIP = '172.31.34.136'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexus' 
    }

    stages{
        stage{'Build'}{
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}