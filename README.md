# my-application
from flask import Flask
app = Flask(__name__)

app_color= 'Blue'

@app.route('/')
def hello():
    return 'Hello, Word!'

@app.route('/user/<username>')
def show_user_profile(username):
    return 'User %s' % escape(username)

@app.route('/post/<int:post_id>')
def show_post(post_id):
    return 'post %d' % post_id

@app.route('/path/<path:subpath>')
def show_subpath(subpath):
    # show the subpath after /path/
    return 'subpath %s' % escape(subpath)
