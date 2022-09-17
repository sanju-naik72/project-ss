pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'sanju'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_GRP_REPO = 'vprofile-maven-group'
        NEXUSIP = '172.31.34.136'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexus' 
    }

    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}