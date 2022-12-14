pipeline {
  agent any
  stages 
{  
    stage ("User Input Stage")
    {
	    
      steps {	 
	      
	 script
         {
            //def choices = ["Docker","Xen","QT"]
	    CHOICES = ["tag1", "tag2", "tag3"];
	    def ChoiceString = CHOICES.join(", ")
	    print ChoiceString
	    env.feature = input message: "Please select a Feature for build" ,   
	                        parameters: [
		   		extendedChoice( defaultValue: 'tag1', description: '', descriptionPropertyValue: 'tag1,tag2,tag3', multiSelectDelimiter: ', ', 
	     			name: 'feature', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: 'ChoiceString', visibleItemCount: 5)
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

