pipeline {
    agent {
  label 'master'
}

stages {
        stage('deploying docker image') {
            steps {		
			sshPublisher(publishers: [sshPublisherDesc(configName: '${Host_name_configured_publish_over_ssh}', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 
			'docker run hello-world', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
			  }
        }
    }
}