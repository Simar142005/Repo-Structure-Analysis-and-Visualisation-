Repository Structure Analysis & Visualization System


Problem Statement

Large software repositories are often difficult to understand because files are interconnected and spread across multiple directories. New contributors usually spend considerable time identifying dependencies and understanding the purpose of each file.

This project provides an automated solution by analyzing a repository, extracting relationships between files, calculating software metrics, and presenting the results through an interactive dependency graph. It also integrates AI-based explanations to make code easier to understand.

Solution

The application combines repository parsing, graph visualization, and generative AI into a single platform.

The system can:

Analyze local projects or public GitHub repositories
Detect relationships between source files
Compute repository statistics
Measure file complexity
Generate AI explanations for individual files
Display the repository as an interactive graph
Project Components
Frontend

The frontend is developed using React and React Flow. It allows users to:

Enter a GitHub repository URL
Explore the dependency graph
View repository statistics
Inspect file information
Generate AI summaries
Backend

The FastAPI backend is responsible for:

Cloning GitHub repositories
Parsing source code
Extracting dependencies
Calculating repository metrics
Communicating with the Gemini API
AI Module

The AI module explains individual source files in simple language by describing:

The file's purpose
Technologies used
Why the file is important

To reduce API usage, summaries are cached and reused whenever the same file is requested again.

Supported File Types

The analyzer currently supports:

Python
JavaScript
React JSX
TypeScript
Java
C
C++
Header files
Jupyter Notebooks
Repository Metrics

For every analyzed file, the system records:

Metric	Description
Lines of Code	Number of executable lines
Complexity	Estimated code complexity
Language	Source language
Dependencies	Imported project files
How the System Works
User
   │
   ▼
Enter GitHub Repository URL
   │
   ▼
Clone Repository
   │
   ▼
Parse Source Files
   │
   ▼
Extract Dependencies
   │
   ▼
Calculate Metrics
   │
   ▼
Generate Graph Data
   │
   ▼
Display Interactive Visualization
   │
   ▼
Generate AI Summary (on node click)
Technology Used
Frontend
React
React Flow
Axios
Vite
Backend
Python
FastAPI
GitPython
Radon
AI Services
Google Gemini API
Installation
Clone Repository
git clone <repository-url>
cd Repository-Structure-Analysis-and-Visualisation-System
Backend
python -m venv venv

source venv/bin/activate

pip install -r requirements.txt

uvicorn app:app --reload

Create a .env file:

GEMINI_API_KEY=YOUR_API_KEY
Frontend
cd frontend

npm install

npm run dev
Future Scope

Possible improvements include:

Automatic graph layout optimization
Repository-wide AI documentation
Advanced search and filtering
Export graph as PNG or PDF
Additional programming language support