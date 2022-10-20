podTemplate(containers: [
    containerTemplate(name: 'k6', image: 'grafana/k6:latest', command: 'sleep', args: '99d')
  ]) {

    node(POD_LABEL) {
        stage('k6') {
            checkout scm
            sh "ls"
            container('k6') {
                stage('test k6') {

                  sh "k6"

                }

    }
        }
    }
  }
