# RAG System For an AI English Teacher

## Watch this youtube video to see the app in action:

[![Watch the video](https://img.youtube.com/vi/2AUnovkePrk/0.jpg)](https://youtu.be/2AUnovkePrk?si=rkT3qud8JtbyMZLa)

## Inspiration:

The inspiration behind Sivi Ai Buddy was to create an interactive, AI-powered tool that helps students study efficiently by providing personalized quiz generation and answering questions from uploaded study materials, like PDFs.The goal was to combine learning with engagement, offering an intelligent way to interact with content and get immediate feedback, which is especially useful in exam preparation or content review.It was motivated by the need to address the problem of passive learning by turning study materials into an active, dynamic process.

## What It Does:

- **Sivi AI Buddy** allows users to upload PDFs (such as textbooks or lecture notes) and asks questions based on the content.
- It generates 10 multiple-choice questions with real-time feedback on correctness and explains why a specific answer is correct or incorrect.
- Users can also ask custom questions about the document, and the system retrieves relevant sections of the text to answer these questions using AI, enhancing comprehension.
- It offers a visually engaging user experience with features like a typewriter effect for text and a streamlined interface.
- The Sivi AI Buddy includes a video transcript summarizer to condense key points from educational videos.
- It also features a screenshot analyzer to extract and analyze content from images for enhanced learning.

## How can We Make This Even Better?
- We can use a more advanced **paid LLM model like GPT-4o and claude 3.5 sonnet** to handle the question answering and quiz generation tasks, which would improve the accuracy and relevance of the responses.
- By using **ollama** locally, we can avoid the token limit issue and improve the speed of the application.
- We can also add more features like chat history, chat summary, and chat export to enhance the user experience and make it more useful for the users.
- Using **openai embeddings**, we can improve the accuracy of the similarity search and retrieval of the most relevant content from the documents.
- Using openai **Realtime API, we can add a voice chat feature to the application**, which would make it more interactive and engaging.

## How I Built It:

- The project was built using Streamlit for the front-end interface, allowing for a user-friendly web app experience.
- LangChain was integrated to manage the workflow for question answering and quiz generation, especially to structure prompts and retrieve relevant document sections using FAISS vector storage.
- Google Generative AI models were used to handle both the conversational aspect for question answering and to generate quizzes based on document content.
- The PyPDF2 library was used to extract and process text from PDF documents, and FAISS was employed for similarity search to retrieve the most relevant content from the documents.
- Various CSS customizations were added for enhanced UI, including animations for better visual engagement.

## Challenges I Ran Into:

- Handling large PDF files and breaking them into chunks that the model could process while keeping the context intact was a significant challenge.
- Integrating different components like LangChain, FAISS, and the Google API to work smoothly together involved overcoming compatibility and embedding issues.
- Managing API token limits and model performance was a challenge when it came to handling larger or more complex documents.
- Ensuring that the quiz questions generated were diverse and challenging enough based on limited content input was another hurdle.

## Accomplishments I Am Proud Of:

- Successfully implemented a Retrieval-Augmented Generation (RAG) system that allows users to get specific, relevant answers from large PDFs.
- Built a dynamic quiz generator that provides users with immediate feedback and explanations, adding to an interactive learning experience.
- Integrated a sleek and engaging UI with custom animations and features like a typewriter effect, making the app more fun and engaging to use.
- Managed to implement a system where users can process complex documents without much delay, thanks to efficient text chunking and retrieval.

## What I Learned:

- Gained experience in building AI-powered applications with a combination of natural language processing, embeddings, and similarity search techniques
- Learned how to work with LangChain for prompt management and chaining tasks, which improved the ability to handle sophisticated workflows.
- Improved understanding of creating seamless interactions between different components like Google's Generative AI, FAISS, and Streamlit to deliver a cohesive user experience.
- Developed problem-solving skills, particularly in overcoming token limits, managing API responses, and integrating multiple systems into one tool.

## What's Next for Study Buddy:
- Expanding to support more file formats (like Word docs or web page scraping) to widen the range of study materials.
- Adding more customizable quiz features, like difficulty levels or topic-based quizzes, to cater to specific user needs.
- Enhancing the user interface with more gamified features like streaks, badges, or study goals to increase user engagement.
- Integrating speech-to-text functionality so that users can ask questions or interact with the app using voice commands.
- Exploring advanced AI features like deeper document summarization or note generation based on uploaded files to enhance the learning experience even further.

## Getting Started

### Prerequisites

- Python 3.9+
- Docker (optional)

### Local Setup

1. Clone the repository:
   ```
   git clone https://github.com/sarvottam-bhagat/RAG-AI-Tutor.git
   cd RAG-AI-Tutor
   ```

2. Create a virtual environment (optional but recommended):
   ```
   conda create -p venv python==3.11 -y
   conda activate venv
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Run the Streamlit app:
   ```
   streamlit run app.py
   ```

5. Open your web browser and navigate to `http://localhost:8501`

### Running with Docker

1. Build the Docker image:
   ```
   docker build -t sivi-app .
   ```

2. Run the Docker container:
   ```
   docker run -p 8501:8501 sivi-app
   ```

3. Open your web browser and navigate to `http://localhost:8501`

## Project Structure

- `app.py`: Main Streamlit application
- `faiss_index`: (Facebook AI Similarity Search) FAISS vector storage for similarity search and clustering of dense vectors.
- `Dockerfile`: Docker configuration for containerization
- `requirements.txt`: Python dependencies
