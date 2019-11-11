properties([
    pipelineTriggers([pollSCM('H/3 * * * *')])
    ])

node(){
    cleanWs()
	
    stage("checkout"){  
      checkout scm
    }

    stage("build"){ 
      sh "make"
      sh "./main"
    }

    stage("archivage"){ 
      archiveArtifacts artifacts: 'main'
    }
}