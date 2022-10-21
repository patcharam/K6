podTemplate(containers: [
        containerTemplate(name: 'k6', image: 'grafana/k6:master', command: 'sleep', args: '99d')
    ]) {
        node(POD_LABEL) {
            container('k6'){
                stage('test k6'){
                
				sh 'k6 version'
				
                }            
        }
    }
}
