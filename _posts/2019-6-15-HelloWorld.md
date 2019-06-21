---
layout: post
title: Testing Helloworld VS Code Extension in Eclipse Che as a Remote Plugin
comments: true
---

Step1: Use command “npm install -g yo generator-code" to generate the helloworld extension with its boilerplate code.  
  
 ![_config.yml]({{ site.baseurl }}/images/blog3-img1.png)  

Step 2: Specify all the details like identifier, description etc. for your extension.  
  
 ![_config.yml]({{ site.baseurl }}/images/blog3-img2.png)  

Step 3: Once your extension is generated you can navigate to your extension directory “helloworld”  
  
![_config.yml]({{ site.baseurl }}/images/blog3-img3.png)  
  
![_config.yml]({{ site.baseurl }}/images/blog3-img4.png)
  

Step 4a: Use the below command to build your extension  
yarn && echo -e "\e[32mDone.\e[0m build ... hello-world-extension-remote-plugin"  
  
 ![_config.yml]({{ site.baseurl }}/images/blog3-img5.png)  

Step 4b: Use the “helloworld” container and use CTRL+SHIFT+P to open command view and then use command “Hosted plugin:start instance”.  
  
![_config.yml]({{ site.baseurl }}/images/blog3-img6.png)    
  
Step 5: Select the path to your helloworld extension.  
  
![_config.yml]({{ site.baseurl }}/images/blog3-img7.png)   
This will launch hosted instance server in another window.  
  
Step 6: use CTRL+SHIFT+P to open command view and use your Helloworld command to test your vs code extension.      
  
![_config.yml]({{ site.baseurl }}/images/blog3-img8.png)
  
  
![_config.yml]({{ site.baseurl }}/images/blog3-img9.png) 

