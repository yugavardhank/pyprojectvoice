# Set up OpenAI API key
import os
from openai import OpenAI

client = OpenAI(
    # This is the default and can be omitted
    api_key=os.environ.get("sk-proj-zJSNyAq3YuBY9jZXiLYsT3BlbkFJWeeT19JD64ndU0kLSty5"),
)

chat_completion = client.chat.completions.create(
    messages=[
        {
            "role": "user",
            "content": "Say this is a test",
        }
    ],
    model="gpt-3.5-turbo",
)