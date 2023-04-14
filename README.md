# WebChatbot
Web implemented chatbot using Flask and Chatterbot<br />
-> Flask is a Web framework used for developing web applications without the need of particular tools or libraries.<br />
-> ChatterBot is a Python library that makes it easy to generate automated responses to a user’s input.
ChatterBot uses a selection of machine learning algorithms to produce different types of responses. This
makes it easy for developers to create chat bots and automate conversations with users. Example:<br />
  user: Good morning! How are you?<br />
  bot: I am good, thank you for asking.<br />
  user: You are welcome.<br />
  bot: Do you like programming?<br />
The chatbot was uploaded on an AWS Ubuntu EC2 instance which launches a webpage where any user with the link can interract with the chatbot.
Can be launched locally by running the app.py from the repository. 
Implementation was done according to: https://medium.com/techfront/step-by-step-visual-guide-on-deploying-a-flask-application-on-aws-ec2-8e3e8b82c4f7
with the following modifications:<br />
1.File 'app.py', app = Flask(__name__, template_folder='Templates')  <br />
2.Chatterbot: a 'py.yaml' dependency has a bug -> adapt from collection.hashtable into collection.abs.hashtable<br />
3.NGINX file - add location /get {proxy_pass: http:/flaskhelloworld/get; }<br />
 
