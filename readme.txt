# Task 1 (Chrome extension)
## Tech Stack
      -HTML
      -CSS
      -JavaScript
      -Express Js
      -Render (to deploy the backend)


## Instruction to run the code
      . Go to Manage Extension
      . Enable the Developer mode
      . Click on the Load unpacked option
      . Select the desired folder of the chrome extension
      . Then, click on the icon of the extension to run the extension


## Limitation of the Extension
      . As, suggest in the pdf to use the pyiodide, it will work for normal site other extension, but as we use in the extenion (due to high security) extension does not allow the script or CDN of the pyiodide to run will be blocked and show CSP error (Content Security Policy)
      . After, 1.5 days  I can't able to find the solution of the error so, That's why I have use other libarary
      . Also, the npm package of pyiodide, is small but needed the whole build file to run (200+mb), this is will make the site more heavy, that's why I havn't use it,
      



## How the code works
      . In the code backend is of express and with compilex npm package to compile the code of the python. 
      . After clicking the python script it will redirect to a site where we can write our code and run it.
      


## Approch to solve

      . Read the docs of the pyiodide to able to use it.
      
      . At, initial it works well on the static sites, After shifting in extension it cause errors and problem
      Then, after around 1.5 day i have to use another source in order to compile the python code.
      Tried many package but main problem on the package is it will generate a python file and excute of the compiler engine that is install in our system. It means that there should python install in the system in order to run it.
      Which make it irrelavent to use an extension if, I have python in my system. (Also tried API from RapidAPI but response time is slow and limited calls available) 

      . Final approach came to use npm package compiler-api which have unlimited calling so, made backend with that and host in render and fetch the backend in order compile my python code.
      
