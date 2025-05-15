This project is an AI-powered chatbot built using Microsoft's DialoGPT-small model and deployed with Gradio. It also demonstrates how to use Hugging Face Inference API to connect to larger models like zephyr-7b-beta.

🚀 Features
Interactive chatbot UI using Gradio

Uses pretrained DialoGPT for generating conversational responses

Integrates with Hugging Face Hub via API tokens

Can be deployed on Hugging Face Spaces

Clean, minimal Python setup — easy to extend

🧠 Model Used
Model	Description
microsoft/DialoGPT-small	A small, conversational transformer trained on Reddit dialogues
HuggingFaceH4/zephyr-7b-beta	(Optional) Large model used via Hugging Face Inference API

📦 Requirements
Install all necessary dependencies using pip:

bash
Copy
Edit
pip install transformers torch gradio huggingface_hub
🧪 How to Run
✅ Local Execution
bash
Copy
Edit
python app.py
Gradio will provide a link like http://127.0.0.1:7860/ in your terminal to interact with the chatbot.

☁️ Deployment on Hugging Face Spaces
Go to Hugging Face Spaces

Click Create New Space

Select Gradio as the SDK

Upload the following files:

app.py (your main code)

requirements.txt

README.md

Add your token as a secret environment variable:

Go to your Space > Settings > Secrets

Add a new secret:

makefile
Copy
Edit
Name: space-token
Value: your_token_here
📁 Project Structure
bash
Copy
Edit
sentimental-analysis-project/
│
├── app.py                 # Main chatbot script
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
🔐 Token Handling
This project uses the huggingface_hub API which requires authentication via token.

python
Copy
Edit
import os
token = os.getenv("space-token")
✅ Best Practice: Store your token as an environment variable and never hardcode it in public projects.

🛠 Future Improvements
Add support for other tasks like sentiment analysis

Store and display chat history

Enable multi-turn conversation with user-side UI improvements

Deploy using Streamlit or as a mobile app
✅ requirements.txt
shell
Copy
Edit
transformers>=4.36.0
torch>=2.1.0
gradio>=4.0.0
huggingface_hub>=0.20.0
📌 Optional Notes:
These versions ensure compatibility with DialoGPT, Gradio, and InferenceClient.

You can add python-dotenv if you want to manage your API keys using a .env file:

shell
Copy
Edit
python-dotenv>=1.0.0
To install all dependencies:

bash
Copy
Edit
pip install -r requirements.txt


📜 License
This project is open-source and licensed under the MIT License.

🙋‍♀️ Author
Developed by Nidhi Tiwari S



