pipeline {
    agent any
    stages {
        stage('Restore dependencies') {
            steps {
                echo 'dotnet restore'
            }
        }
        stage('Build dotnet app') {
            steps {
                echo 'dotnet build --no-restore'
            }
        }
        stage('Run unit tests') {
            steps {
              echo 'dotnet test Homies.Tests/Homies.Tests.csproj --no-build --verbosity normal'            }
        }
        stage('Run integration tests') {
            steps {
                echo 'dotnet test Homies.IntegrationTests/Homies.IntegrationTests.csproj --no-build --verbosity normal'
            }
        }
    }
}
