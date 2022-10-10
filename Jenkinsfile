pipeline{
      agent any
      tools{
            maven 'MAVEN3.8.6'
            jdk 'JDK8'
      }
      environment{
        SNAP_REPO= 'prem-sanpshot'
        NEXUS_USER= 'admin'
        NEXUS_PASS= '12345'
        RELEASE_REPO= 'prem-pro'
        CENTRAL_REPO= 'prem-maven-proxy'
        NEXUSIP= '172.31.14.178'
        NEXUSPORT= '8081'
        NEXUS_GRP_REPO= 'prem-maven-group'
        NEXUS_LOGIN= 'Nexusrepository'

      }
      stages{
            stage('Build'){
                steps{
                    sh 'mvn -s settings.xml -DskipTest install'
                }
            }
      }
}