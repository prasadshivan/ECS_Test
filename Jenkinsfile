pipeline {
  agent any
  parameters {
    string(name: 'REPONAME', defaultValue: 'example/nginx', description: 'AWS ECR Repository Name')
    string(name: 'ECR', defaultValue: '447895454160.dkr.ecr.us-east-1.amazonaws.com/example/nginx', description: 'AWS ECR Registry URI')
    string(name: 'REGION', defaultValue: 'us-east-1', description: 'AWS Region code')
    string(name: 'CLUSTER', defaultValue: 'DevopsTest', description: 'AWS ECS Cluster name')
    string(name: 'TASK', defaultValue: 'ExampleTask', description: 'AWS ECS Task name')
  }
  stages {
    
    stage('DeployStage') {
      steps {
        sh 'aws ecs list-task-definitions --family-prefix ExampleTask'
      }
    }
   
  }
}
