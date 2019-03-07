node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t oscar_test:latest ."
}

stage('Docker login to hub and '){
sh "docker login -u 'omwale' -p 'Justlaugh@2019' "


}
stage('Docker tag') {
sh "docker tag oscar_test:latest omwale/oscar_test:latest"
}
stage('push the image') {
sh "docker push omwale/oscar_test:latest"
}
stage('Apply changes to the environment') {
sh "ls -l"
}


}
