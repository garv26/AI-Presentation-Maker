OpenAI PowerPoint Presentation Generator
This is a Python script that uses OpenAI's GPT-3 API to automatically generate PowerPoint presentations on a given topic.

Usage
Sign up for an OpenAI account and get an API key.
Add your API key to the api_key variable in the script.
Run the script using streamlit run PPT_Generator.py.
Enter a topic and number of slides when prompted.
The script will generate a PowerPoint presentation called {topic}_presentation.pptx.
Overview
The script uses the following main components:

Streamlit for the UI to get user input.
OpenAI API with the gpt-3.5-turbo-instruct model to generate subtopics and content for each slide.
Python-PPTX to create the actual PowerPoint presentation.
For each slide, it first generates a subtopic related to the main topic using OpenAI. It then generates 50 words or bullet points of content for that subtopic.

The script limits the number of slides to a maximum of 10 to avoid hitting OpenAI token limits. It also adds a delay between API requests to stay within the rate limits.

Customization
Adjust the max_tokens parameters for Completion.create() to control length of generated text.
Modify the prompt templates for subtopics and content to tailor the style.
Change the slide layout as needed by using different slide_layouts.
Adjust the rate limiting sleep duration based on your API limits.
