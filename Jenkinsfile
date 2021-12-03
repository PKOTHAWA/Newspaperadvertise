pipeline{

agent any



stages {

stage('Verify Branch'){

steps{

echo "@GIT_BRANCH"



}

}

stage('Checkout'){

steps{

git branch: 'main', url: 'https://github.com/PKOTHAWA/Newspaperadvertise.git'

}

}

stage('Build'){

steps{

bat 'mvn compile'

}

}

stage('Package'){

steps{

bat 'mvn package'

}

}









}

}
 	 
