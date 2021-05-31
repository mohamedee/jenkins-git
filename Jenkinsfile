pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh curl -X POST --insecure -H "Authorization: Bearer eyJrIjoiSlRFWWhkaGFvSzZ2WHY4NldKVjRpQUNmSmxFQjJMcE4iLCJuIjoiYXBpa2V5Y3VybCIsImlkIjoxfQ==" -H "Content-Type: application/json" -d @dashboard.json http://admin:ryfsp1WzchgknU1pPrghxYT4GbQVjGEjm5SDDT3G@34.75.79.251:30005/api/dashboards/db
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
