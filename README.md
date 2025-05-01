<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Video Summary API - README</title>
</head>
<body>
  <h1>🎥 Video Summary API</h1>
  <p><strong>FastAPI-based service to summarize YouTube videos and uploaded video files using OpenAI, NLTK, LangChain, and more.</strong></p>

  <h2>🚀 Features</h2>
  <ul>
    <li>Summarize YouTube videos by URL</li>
    <li>Summarize uploaded video files (e.g., MP4)</li>
    <li>Multiple summary formats: <code>markdown</code>, <code>bullet</code>, <code>narrative</code></li>
    <li>Adjustable summary length: <code>short</code>, <code>medium</code>, <code>long</code></li>
    <li>Supports multiple languages (translation)</li>
    <li>Optional sentiment analysis using NLTK</li>
    <li>Keyword extraction from transcript</li>
    <li>Stores summaries with metadata</li>
  </ul>

  <h2>🧠 Tech Stack</h2>
  <ul>
    <li><strong>FastAPI</strong> for building APIs</li>
    <li><strong>LangChain</strong> with <code>ChatOpenAI</code></li>
    <li><strong>MoviePy</strong> + <strong>SpeechRecognition</strong> for audio transcription</li>
    <li><strong>YouTubeTranscriptAPI</strong> and <strong>pytube</strong> for YouTube data</li>
    <li><strong>NLTK</strong> for sentiment analysis</li>
    <li><strong>dotenv</strong> for API key management</li>
  </ul>

  <h2>📦 Installation</h2>
  <pre>
git clone https://github.com/yourusername/video-summary-api.git
cd video-summary-api
pip install -r requirements.txt
  </pre>

  <h2>🔑 Setup</h2>
  <p>Create a <code>.env</code> file and add your OpenAI API key:</p>
  <pre>
OPENAI_API_KEY=your_openai_api_key
  </pre>

  <h2>▶️ Running the Server</h2>
  <pre>
uvicorn main:app --reload
  </pre>

  <h2>📡 API Endpoints</h2>
  <ul>
    <li><code>POST /summarize/youtube</code> - Summarize a YouTube video</li>
    <li><code>POST /summarize/upload</code> - Upload and summarize a local video</li>
    <li><code>GET /summaries</code> - Get all summaries</li>
    <li><code>GET /summaries/{id}</code> - Get a specific summary</li>
    <li><code>DELETE /summaries/{id}</code> - Delete a summary</li>
  </ul>

  <h3>📝 Example: Summarize a YouTube Video</h3>
  <pre>
POST /summarize/youtube
{
  "url": "https://www.youtube.com/watch?v=your_video_id",
  "options": {
    "format": "markdown",
    "length": "medium",
    "language": "english",
    "include_sentiment": true,
    "include_keywords": true
  }
}
  </pre>

  <h2>📄 License</h2>
  <p>This project is licensed under the MIT License.</p>

  <h2>🙌 Author</h2>
  <p>Developed by <strong>Prince katiyar</strong>. Contributions are welcome!</p>
</body>
</html>
