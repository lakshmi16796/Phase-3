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
	    String x = "Hello";
	    env.feature = input message: "Please select a Feature for build" ,   
	                        parameters: [
		   		extendedChoice( defaultValue: 'Docker', description: '', descriptionPropertyValue: 'Docker,Xen,QT', multiSelectDelimiter: ',', 
	     			name: 'feature', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: ${x}, visibleItemCount: 5)
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

