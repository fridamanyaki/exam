node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t examrepo:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'fmanyaki' -p 'j3nk1nss' "
sh "docker tag examrepo:latest fridahmanyaki/examrepo:latest"
sh "docker push fridahmanyaki/examrepo:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}

