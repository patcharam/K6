podTemplate(containers: [
    containerTemplate(name: 'ubuntu', image: 'ubuntu:latest', command: 'sleep', args: '99d')
  ]) {

    node(POD_LABEL) {
        container('ubuntu') {
            stage('POC') {

                sh '''
                apt-get update
                apt-get install -y dirmngr --install-recommends
                apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C5AD17C747E3415A3642D57D77C6C491D6AC1D69
                echo "deb https://dl.k6.io/deb stable main" | tee /etc/apt/sources.list.d/k6.list
                apt-get update
                apt-get install -y k6'

                k6 version 
                '''

            }
            
        }
    }
}
