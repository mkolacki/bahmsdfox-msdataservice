node {
    stage ("Checkout DataService"){
        git branch: 'main', url: ' https://github.com/foxwas/bahmsdfox-msdataservice.git'
    }
    
    stage ("Gradle Build - DataService") {
        bat'gradle clean build'
    }
    
    stage ("Gradle Bootjar-Package - DataService") {
        bat 'gradle bootjar'
    }
    
    stage('User Acceptance Test - DataService') {
	
	  def response= input message: 'Is this build good to go?',
	   parameters: [choice(choices: 'Yes\nNo', 
	   description: '', name: 'Pass')]
	
	  if(response=="Yes") {
	    stage('Release - DataService') {
	      bat 'gradle build -x test'
	      bat 'echo Release this version'
	    }
	  }
    }
}
