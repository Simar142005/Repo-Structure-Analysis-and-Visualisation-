🚀 Repository Structure Analysis & Visualization System

A full-stack software architecture analysis platform that automatically parses local and GitHub repositories, constructs dependency graphs, computes code metrics, and generates AI-powered code summaries for improved repository comprehension.

📌 Overview

Modern software repositories often contain hundreds of interconnected files, making onboarding and architecture understanding difficult.

The Repository Structure Analysis & Visualization System addresses this problem by automatically:

Parsing source code repositories
Extracting dependency relationships
Computing code metrics (LOC & Complexity)
Generating interactive dependency graphs
Producing AI-powered file summaries
Optimizing repeated AI calls through cache-based inference
The platform enables developers to quickly understand unfamiliar codebases and visualize repository architecture.

✨ Features
Repository Analysis
Analyze local repositories
Analyze public GitHub repositories
Automatic repository cloning and parsing
Dependency Graph Visualization
Interactive graph-based architecture visualization
Dependency relationship mapping
Complexity-based node coloring
React Flow powered visualization
Code Metrics
Lines of Code (LOC)
Cyclomatic Complexity (Python)
Heuristic Complexity Estimation (JS, TS, Java, C, C++)
Repository Statistics Dashboard
AI-Powered Insights
File-level AI summaries using Gemini API
Click-to-summarize functionality
Cache-based summary optimization
Reduced redundant LLM requests
Multi-Language Support
Python (.py)
Jupyter Notebooks (.ipynb)
JavaScript (.js)
React (.jsx)
TypeScript (.ts)
TSX (.tsx)
Java (.java)
C (.c)
C++ (.cpp, .hpp, .h)
User Experience
Light/Dark Theme
Interactive Node Inspection
Real-Time Repository Visualization
🏗️ System Architecture

⚙️ Technology Stack
Frontend
Technology	Purpose
React	User Interface
React Flow	Graph Visualization
Axios	API Communication
Backend
Technology	Purpose
FastAPI	REST API Backend
Python	Repository Analysis
GitPython	GitHub Repository Cloning
AI Layer
Technology	Purpose
Gemini API	AI Code Summarization
🔄 Workflow
User submits a GitHub repository URL.
Backend clones and analyzes the repository.
Source files are parsed.
Dependency relationships are extracted.
LOC and complexity metrics are computed.
Graph data is generated.
React Flow visualizes repository architecture.
User clicks a file node.
Gemini generates an AI summary.
Summary is cached for future requests.
📊 Complexity Analysis Strategy
Python
Cyclomatic Complexity is calculated using Radon.

Other Languages
Complexity is estimated using decision-point heuristics:

if
else
for
while
switch
case
catch
try
This provides meaningful complexity estimation across multiple languages while maintaining fast analysis speed.

🧠 Cache Optimization
To reduce redundant LLM requests:

File hashes are generated
Previously summarized files are cached
Repeated requests return cached summaries
Reduces API costs and latency
Example:

CACHE MISS → Generate Summary → Save Cache
CACHE HIT  → Return Cached Summary
🚀 Installation
Backend
🚀 Installation & Setup
1. Clone the Repository
git clone https://github.com/Urahara0723/Repository-Structure-Analysis-and-Visualisation-System.git

cd Repository-Structure-Analysis-and-Visualisation-System
2. Backend Setup
Create and activate a virtual environment:

python -m venv venv
Windows
venv\Scripts\activate
Linux / macOS
source venv/bin/activate
Install dependencies:

pip install -r requirements.txt
Create a .env file:

GEMINI_API_KEY=your_api_key_here
Start the FastAPI server:

uvicorn app:app --reload
Backend runs at:

http://127.0.0.1:8000
3. Frontend Setup
Open a new terminal:

cd frontend
Install dependencies:

npm install
Start the development server:

npm run dev
Frontend runs at:

http://localhost:5173
4. Using the Application
Open http://localhost:5173
Paste a public GitHub repository URL
Click Analyze GitHub Repo
Explore the dependency graph
Click any node to generate an AI summary
Toggle between Light and Dark mode
Example Repositories
https://github.com/axios/axios

https://github.com/google/googletest

https://github.com/pallets/flask
