# Task 1 (Chrome extension)
## Tech Stack
<ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
      <li>Express Js</li>
      <li>Render (to deploy the backend)</li>
</ul>

## Instruction to run the code
<ul>
      <li>Go to Manage Extension</li>
      <li>Enable the Developer mode</li>
      <li>Click on the Load unpacked option</li>
      <li>Select the desired folder of the chrome extension</li>
      <li>Then, click on the icon of the extension to run the extension</li>
</ul>

## Limitation of the Extension
<ul>
      <li>
      <i>
      As, suggest in the pdf to use the pyiodide, it will work for normal site other extension, but as we use in the extenion (due to high security) extension does not allow the script or CDN of the pyiodide to run will be blocked and show CSP error (Content Security Policy)
      </i>
      </li>
      <li>
      <i>
      After, 1.5 days  I can't able to find the solution of the error so, That's why I have use other libarary
      </i>
      </li>
            <li>
      <i>
      Also, the npm package of pyiodide, is small but needed the whole build file to run (200+mb), this is will make the site more heavy, that's why I havn't use it,
      </i>
      </li>
</ul>


## How the code works
<ul>
      <li>In the code backend is of express and with compilex npm     package to compile the code of the python.
      </li>
      <li>After clicking the python script it will redirect to a site where we can write our code and run it.
      </li>
</ul>

## Approch to solve
<ul>
      <li>Read the docs of the pyiodide to able to use it.
      </li>
      <li>At, initial it works well on the static sites, After shifting in extension it cause errors and problem</li>
      <li>Then, after around 1.5 day i have to use another source in order to compile the python code.</li>
      <li>Tried many package but main problem on the package is it will generate a python file and excute of the compiler engine that is install in our system. It means that there should python install in the system in order to run it.</li>
      <li>Which make it irrelavent to use an extension if, I have python in my system. (Also tried API from RapidAPI but response time is slow and limited calls available) 
      </li>
      <li>
            Final approach came to use npm package compiler-api which have unlimited calling so, made backend with that and host in render and fetch the backend in order compile my python code.
      </li>
</ul>