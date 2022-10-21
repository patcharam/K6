podTemplate(containers: [
        containerTemplate(name: 'k6', image: 'loadimpact/k6:latest', command: 'sleep', args: '99d')
    ]) {
        node(POD_LABEL) {
            container('k6'){
                stage('test k6'){
                
				sh 'k6 version'
				
                }            
        }
    }
}
