stage "DEV-QA"

node {
    git 'https://github.com/Sunny-Dee/se441-qotd.git'
    
    def gradleHome = tool 'Gradle2.9'
    sh "${gradleHome}/bin/gradle.sh assemble uploadArchives"
    
    step([$class: 'ArtifactArchiver', artifacts:'**/*.war', fingerprint: true])
}