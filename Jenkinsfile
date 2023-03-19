pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script{
                    currStageName = "Build"
                }
                echo '${currStageName} - START'
                echo '${currStageName} - END'                
            }
        }
        stage('deployTimeout') {
            steps {
                snDevOpsChange changeCreationTimeOut: 40, changeRequestDetails: '{ "attributes": { "short_description": "Test description", "priority": "1", "start_date": "2021-02-05 08:00:00", "end_date": "2022-04-05 08:00:00", "justification": "test justification", "description": "test description", "cab_required": true, "comments": "This update for work notes is from jenkins file", "work_notes": "test work notes", "assignment_group": "a715cd759f2002002920bde8132e7018" }, "setCloseCode": false }', changeStepTimeOut: 60, pollingInterval: 5
                echo 'change with timeout'
                
            }
        }
        stage('postDeploy') {
            steps {
                echo 'post deploy'                
            }
        }
    }
}

