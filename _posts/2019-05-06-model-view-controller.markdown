---
layout: post
title:      "Model-View-Controller"
date:       2019-05-06 14:36:27 +0000
permalink:  model-view-controller
---


I am going to write about the Model View Controller (MVC) pattern. This pattern is key to getting everything to function properly on a web page and I think it's fascinating! Not only is it really interesting, it's absolutely key to the whole user experience. If your Models are not communicating well with your Controllers, the Views will be broken. And the cycle just continues.

The Models work with all the data and logical components. It is then transferred between the Views and Controllers so they can either be displayed to the user via views or communicated by the controller. 

The Views are the component that will display user interface (UI). So, the views will take everything it heard from the model and display that. What sort of characteristics have been defined by the model, etc. 

Finally, the Controllers act as an interface between Model and View components to process all of the buisness logic and incoming requests, will manipulate the data using the Model component and interact with the Views to develop the final ouput. 

Properly setting up your MVC is the most important part of this whole process. Otherwise you will get errors right and left since all of these files interconnected!
