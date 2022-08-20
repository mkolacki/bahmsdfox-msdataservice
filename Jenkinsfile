node {
    stage ("Checkout DataService"){
        git branch: 'main', url: ' https://github.com/foxwas/bahmsdfox-msdataservice.git'
    }
    
    stage ("Gradle Build - DataService") {
<<<<<<< HEAD
        sh'gradle clean build'
=======
        sh 'gradle clean build'
>>>>>>> 197917d9aad214f7047c1350e9cc2e01927afee7
    }
    
    stage ("Gradle Bootjar-Package - DataService") {
        sh 'gradle bootjar'
    }
    
    stage('User Acceptance Test - DataService') {
	
	  def response= input message: 'Is this build good to go?',
	   parameters: [choice(choices: 'Yes\nNo', 
	   description: '', name: 'Pass')]
	
	  if(response=="Yes") {
<<<<<<< HEAD
	    stage('Release- DataService') {
	      sh 'gradle build -x test'
	      sh 'echo DataService is ready to release!'
=======
	    stage('Release - DataService') {
	      sh 'gradle build -x test'
	      sh 'echo Release this version'
>>>>>>> 197917d9aad214f7047c1350e9cc2e01927afee7
	    }
	  }
    }
}
