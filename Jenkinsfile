pipeline{
  agentanystages{
    stage('build'){
      steps{
        sh 'javac-d.src/*.java'sh'echoMain-Class: Rectangulator>MANIFEST.MF'sh'jar-cvmfMANIFEST.MFrectangle.jar*.class'
      }post{
        success{
          archiveArtifactsartifacts: 'rectangle.jar',
          fingerprint: true
        }
      }
    }stage('run'){
      steps{
        sh'java-jarrectangle.jar79'
      }
    }stage('PromoteDevelopmenttoMaster'){
      when{
        branch'development'
      }steps{
        echo'StashingLocalChanges'sh'gitstash'echo'CheckingOutDevelopment'sh'gitcheckoutdevelopment'sh'gitpullorigin'echo'CheckingOutMaster'sh'gitcheckoutmaster'echo'MergingDevelopmentintoMaster'sh'gitmergedevelopment'echo'GitPushtoOrigin'sh'gitpushoriginmaster'
      }
    }
  }
}