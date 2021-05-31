pipeline {
    agent any
  
    stages {
        stage('Build') {
            steps {
                
                  script {
            def props = readProperties file: 'vars.properties'
            env = props
                      }
                sh "echo The weather is ${env.WEATHER}"
                sh 'curl -X POST --insecure -H "Authorization: Bearer eyJrIjoiSlRFWWhkaGFvSzZ2WHY4NldKVjRpQUNmSmxFQjJMcE4iLCJuIjoiYXBpa2V5Y3VybCIsImlkIjoxfQ==" -H "Content-Type: application/json" -d @dashboard.json http://admin:ryfsp1WzchgknU1pPrghxYT4GbQVjGEjm5SDDT3G@$IP:$PORT/api/dashboards/db'
                sh '''
                    echo "Multiline shell steps works too yes!  "
                    ls -lah
                '''
            }
        }
    }
}
