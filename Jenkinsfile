pipeline {
    agent any
    // Добавляем триггер для активации по коммиту в Git
    triggers {
        pollSCM('* * * * *')  // Проверяет изменения каждую минуту (для теста)
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo "This pipeline was triggered by a Git commit!"'
                sh 'echo "Current branch: $GIT_BRANCH"'
            }
        }
    }
}
