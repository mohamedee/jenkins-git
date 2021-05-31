pipeline {
    agent any
    environment {
        GRAFANA_ACCESS_BEARER   = credentials('GRAFANA_ACCESS_BEARER')
        GRAFANA_USERNAME = credentials('GRAFANA_USERNAME')
        GRAFANA_PASSWORD = credentials('GRAFANA_PASSWORD')
    }
  
    stages {
        stage('Build') {
            steps {
                
                  script {
            def props = readProperties file: 'vars.properties'
            env = props
                      }
                sh "echo The weather is ${env.GRAFANA_ACCESS_BEARER}"
                sh "curl -X POST --insecure -H 'Authorization: Bearer eyJrIjoiSlRFWWhkaGFvSzZ2WHY4NldKVjRpQUNmSmxFQjJMcE4iLCJuIjoiYXBpa2V5Y3VybCIsImlkIjoxfQ==' -H 'Content-Type: application/json' -d @dashboard.json http://admin:ryfsp1WzchgknU1pPrghxYT4GbQVjGEjm5SDDT3G@${env.IP}:${env.PORT}/api/dashboards/db"
                sh '''
                    echo "Multiline shell steps works too yes!  "
                    ls -lah
                '''
            }
        }
    }
}
