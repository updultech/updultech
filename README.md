
👋 Hi, I’m @updultech
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=updultech&show_icons=true&theme=radical)
![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=updultech&theme=radical)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=updultech&layout=compact&theme=radical)
### 🛠️ Languages and Tools
<p>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="40"/> 
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="40"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" width="40"/>
</p>
![Profile Views](https://komarev.com/ghpvc/?username=updultechE&color=blue)  





- 
- 👀 I’m interested in data science and analytics and  web development...
- 🌱 I’m currently learning ...python,SQL,css and javascript
- 
- 💞️ I’m looking to collaborate on real world projects that are data science and analytics based or web development based projects..
- 📫 How to reach me @wise03667@gmail.com...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...from flask import Flask, request, jsonify
import re

app = Flask(__name__)

# Define a regular expression for strong password validation
# A strong password has at least:
# - 8 characters
# - one uppercase letter
# - one lowercase letter
# - one digit
# - one special character
password_regex = re.compile(r'^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$')

def is_strong_password(password):
    return bool(password_regex.match(password))

@app.route('/signup', methods=['POST'])
def signup():
    data = request.get_json()
    
    username = data.get('username')
    password = data.get('password')
    
    if not username or not password:
        return jsonify({'error': 'Username and password are required'}), 400
    
    if not is_strong_password(password):
        return jsonify({'error': 'Password is not strong enough'}), 400
    
    # Here you would normally save the user to your database
    # For this example, we just return a success message
    return jsonify({'message': 'User signed up successfully'}), 200

if __name__ == '__main__':
    app.run(debug=True)        

<!---
updultech/updultech is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
