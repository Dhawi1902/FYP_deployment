# FYP_deployment

follow the step from this youtube video
https://youtu.be/CSEmUmkfb8Q?si=qGXlXr53ADgrAWbw

github link from the video
https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbHRSajAyaVRIcXBhN3I5b0ZpbE1nMUhmUF93UXxBQ3Jtc0trZ3RQRS1Ienl1VEJfVHB1a2hoMmxNZ3NXRlpYUUVBczJGSm9EbGhrSTJEM3lsT2ZGa1JCeW9McWNXV2paRThHaFVPX3lCRS1QSkY3bEJ5ZmtoTUdiUUc2ZEt5WTM0Q3JKYlRVYUlITGFJcF9xc216Zw&q=https%3A%2F%2Fgithub.com%2Fkrishnaik06%2FDeployment-Deep-Learning-Model&v=CSEmUmkfb8Q

Once you have successful to run the code, you probably have your drectories like this:
  --direcotries
  
    --deployment
      --static
        --css
        --js
      --template
        --index
        --base
      --app.py

from this point you can prompt ChatGPT to complete or adjust the code according to your project.

###example prompt:
i want to deploy my machine learning models using flask, and this is my current directories:
--deployment
  --static
    --css
    --js
  --template
    --index
    --base
  --app.py

i want to add some new pages:
 --resnet50

this is my base page looks like:
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>AI Demo</title>
    <link href="https://cdn.bootcss.com/bootstrap/4.0.0/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.bootcss.com/popper.js/1.12.9/umd/popper.min.js"></script>
    <script src="https://cdn.bootcss.com/jquery/3.3.1/jquery.min.js"></script>
    <script src="https://cdn.bootcss.com/bootstrap/4.0.0/js/bootstrap.min.js"></script>
    <link href="{{ url_for('static', filename='css/main.css') }}" rel="stylesheet">      
</head>

<body>
    <nav class="navbar navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">AI Demo</a>
            <button class="btn btn-outline-secondary my-2 my-sm-0" type="submit">Help</button>
        </div>
    </nav>
    <div class="container">
        <div id="content" style="margin-top:2em">{% block content %}{% endblock %}</div>
    </div>
</body>

<footer>
    <script src="{{ url_for('static', filename='js/main.js') }}" type="text/javascript"></script>    
</footer>

</html>



###Addtitional notes
- base.html is basically act as base for all other pages. the navbar used from this method is only in base page. the content of this page is only extension from other html file. 
