from flask import Flask, request, render_template_string

app = Flask(__name__)

@app.route('/')
def index():
    user_input = request.args.get('input', 'default')
    # Vulnerable to XSS: unsanitized user input directly in HTML
    html_response = f"<html><body><p>User input: {user_input}</p></body></html>"
    return html_response

if __name__ == '__main__':
    app.run(debug=True)
