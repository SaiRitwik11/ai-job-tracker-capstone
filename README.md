# 📊 AI-Powered Job Application Analytics Tracker

<div align="center">

![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python)
![Gemini](https://img.shields.io/badge/Google-Gemini%202.0-orange?style=for-the-badge&logo=google)
![SQLite](https://img.shields.io/badge/SQLite-Database-green?style=for-the-badge&logo=sqlite)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**An intelligent job application tracking system powered by Google's Gemini AI**

[View Demo](#-sample-output) • [Quick Start](#-quick-start) • [Workshop Coverage](#-workshop-coverage-analysis)

</div>

---

**Developed as part of Google’s AI Agents Intensive Workshop (Kaggle × Google).**

An analytics-focused system designed to track, measure, and optimize job application performance using real-world data.

## 📊 Analytics Perspective 

This project is designed not just as a system, but as an analytics tool to track and optimize job application performance.

Key metrics analyzed:
- Application pipeline conversion rates  
- Response rates by company and role  
- Follow-up timing effectiveness  

The focus is on extracting actionable insights from application data rather than building AI models from scratch.

💡 This project focuses on analyzing job application data to improve conversion rates, optimize follow-ups, and increase interview success probability.

---

## 🎯 Project Overview

This AI agent helps job seekers:
- 📝 Track all applications in one centralized database
- 🔄 Monitor application status and progress
- 🔍 Research companies quickly
- ⏰ Set automated follow-up reminders
- 📊 Visualize job search analytics

### Why This Project?

After months of job hunting with applications scattered across emails, spreadsheets, and sticky notes, I built this intelligent assistant to streamline my job search process. This capstone project demonstrates practical AI agent development while solving a genuine personal challenge.

## ✨ Key Capabilities

- Tracks application pipeline stages and conversion rates  
- Monitors response rates across roles and companies  
- Enables follow-up timing analysis  
- Stores structured application data for analysis  
- Provides dashboard for performance tracking  

## ⚙️ System Design

- AI agent workflow for query handling  
- SQLite-based structured data storage  
- Python-based analytics processing  

## 📓 View the Project Notebook

**🌟 Best Viewing Experience:**
- **[View on Kaggle](https://www.kaggle.com/code/jannusairitwik/ai-job-application-tracker-capstone-project)** - Full interactive notebook with all outputs ⭐ RECOMMENDED
- **[Run Your Own Copy](https://www.kaggle.com/code/jannusairitwik/ai-job-application-tracker-capstone-project/edit)** - Fork and experiment

**Download:**
- [Download .ipynb](https://github.com/SaiRitwik11/ai-job-tracker-capstone/raw/main/ai-job-application-tracker-capstone.ipynb) - Run locally in Jupyter

> **Note**: For the best experience with visualizations and outputs, view on Kaggle. GitHub's notebook renderer has size limitations.

## 🚀 Quick Start

### Prerequisites

```bash
pip install google-generativeai pandas matplotlib seaborn
```

### Setup

1. Clone the repository:
```bash
git clone https://github.com/SaiRitwik11/ai-job-tracker-capstone.git
cd ai-job-tracker-capstone
```

2. Set up your Google API key:
```python
# Option 1: Environment variable
export GOOGLE_API_KEY="your_api_key_here"

# Option 2: Kaggle Secrets (if running on Kaggle)
# Configured automatically
```

3. Run the notebook:
```bash
jupyter notebook ai-job-application-tracker-capstone.ipynb
```

### Usage Examples

```python
# Initialize the agent
agent = JobSearchAgent(use_mock=False)  # Set to True for demo mode

# Save a new application
agent.process_query(
    "I applied to Google for a Software Engineer position in Bangalore"
)

# Check your applications
agent.process_query("Show me all my applications")

# Update status
agent.process_query("Update application #1 to Interviewing")

# Set reminder
agent.process_query("Set a reminder for application #2 in 7 days")

# View statistics
agent.process_query("Show my job search statistics")
```

## 📊 Database Schema

### Applications Table
- Basic info: company, role, location, salary range
- Status tracking: Applied, Interviewing, Assessment, Offer, etc.
- Timestamps: applied_date, last_updated, follow_up_date

### Activity Log
- Complete audit trail of all actions
- Timestamps and detailed descriptions

### Metrics Table
- Performance metrics: response times, success rates
- Quality monitoring data

## 🔍 Key Implementation Details

### Intelligent Query Processing

The agent uses pattern matching (in mock mode) or Gemini's NLU (in API mode) to understand user intent:

```python
# Examples of understood queries:
"I just applied to Microsoft for a Data Scientist role"
"Show me applications with status Interviewing"
"What's my success rate?"
"Remind me to follow up with Amazon in 5 days"
```

### Mock Mode

To demonstrate architecture without consuming API quota:
- Uses pattern matching for query understanding
- Executes real tool functions
- Saves actual data to database
- Perfect for testing and demos

```python
agent = JobSearchAgent(use_mock=True)
```

## 📈 Sample Output

```
🎬 DEMO: Saving Job Applications
════════════════════════════════════════════════════════════════════════

Query: I just applied to Google for SWE in Bangalore
──────────────────────────────────────────────────────────────────────

✅ Response (0.35s):

Got it! I've saved your application:
• Company: Google
• Role: Software Engineer
• Application ID: #1

Good luck! I'll help you track this. 🎯
```

### Analytics Dashboard
   ![Analytics Dashboard](images/dashboard-preview.png)

## 📈 Business Insights

This system helps answer:
- Which applications convert to interviews?
- Which roles have higher response rates?
- When is the best time to follow up?

These insights help improve job search efficiency and decision-making.
```

## 🎓 Workshop Coverage Analysis

### Day 1: Agent Architecture ✅
- Implemented `JobSearchAgent` class with clean separation of concerns
- State management via conversation history
- Query processing pipeline with tool selection

### Day 2: Tool Integration ✅
- 7 fully functional tools with type hints
- Proper function declarations for Gemini
- Error handling and validation

### Day 3: Memory & Context ✅
- SQLite for persistent storage
- Activity logging for complete audit trail
- Conversation history maintenance

### Day 4: Quality & Evaluation ✅
- Response time tracking
- Success rate calculation
- Tool usage analytics
- Built-in metrics system

### Day 5: Production Ready ✅
- Comprehensive error handling with logging
- Rate limiting considerations
- Database connection management
- Graceful degradation (mock mode)

## 🔮 Future Enhancements

- [ ] Email integration for automated follow-ups
- [ ] Calendar sync for interview scheduling
- [ ] Advanced analytics with ML predictions
- [ ] Web interface using Streamlit/Flask
- [ ] Export to PDF/Excel reports
- [ ] Integration with job boards (LinkedIn, Indeed)
- [ ] Resume tailoring suggestions

---

## 📬 Contact

**Jannu Sai Ritwik**

- LinkedIn: https://www.linkedin.com/in/jannu-sai-ritwik-339749201/
- Email: sairitwik008@gmail.com
- Kaggle:(https://www.kaggle.com/jannusairitwik)

---

## 🤝 Contributing

This is a capstone project, but suggestions and improvements are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

**Jannu Sai Ritwik**

- Workshop: Google AI Agents Intensive (5 Days)
- Date: November 2025
- Project: AI Job Application Tracker Capstone

## 🙏 Acknowledgments

- Google AI Agents Workshop organizers and instructors
- Google Gemini API team
- Kaggle platform for hosting and compute resources
- Fellow workshop participants for inspiration
---

<div align="center">

### ⭐ If you found this project helpful, please consider giving it a star!

**Built with ❤️ during the Google AI Agents 5-Day Workshop**

</div>
```
