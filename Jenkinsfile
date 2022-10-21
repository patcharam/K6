podTemplate(containers: [
    containerTemplate(name: 'ubuntu', image: 'ubuntu:latest', command: 'sleep', args: '99d')
  ]) {

    node(POD_LABEL) {
        container('ubuntu') {
            stage('POC') {

                sh """
                apt-get update

                gpg --no-default-keyring --keyring /usr/share/keyrings/k6-archive-keyring.gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C5AD17C747E3415A3642D57D77C6C491D6AC1D69
                echo "deb [signed-by=/usr/share/keyrings/k6-archive-keyring.gpg] https://dl.k6.io/deb stable main" | tee /etc/apt/sources.list.d/k6.list
                apt-get update
                apt-get install k6

                k6 version 
                """

            }
            
        }
    }
}
