pipeline {
  agent any
  stages 
{  
    stage ("User Input Stage")
    {
	    
      steps {	 
	      
	      script {
		
            echo "selected parameter is"		      
	    echo "${env.choices}"	      
	    CHOICES = ["tag1","tag2","tag3"];
	    String ChoiceString = CHOICES.join(",")
	    String s1 = "Docker,Xen,QT"
	 
	    print ChoiceString
	    env.feature = input message: "Please select a Feature for build" ,   
	                        parameters: [
		   		extendedChoice( defaultValue: 'Docker', description: '', descriptionPropertyValue: 'Docker,Xen,QT', multiSelectDelimiter: ',', 
	     			name: 'feature', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: '{s1}', visibleItemCount: 5)
               		        ]
	    echo "Selected feature is ${feature}"
		 
        echo "Entered feature is "
	echo "${env.feature}"
	

	
	dir("/home/lakshmi/dell_pods/poky/build/conf")  {
        sh '''#!/bin/bash
	input=$(printenv feature)
	echo "your input"
	echo "$input"
	'''
	}
} 
  }
  }
  }
  
  }

