# ⚡ EV Range Predictor

**AI-Powered Electric Vehicle Range Prediction System**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.51.0-red)](https://streamlit.io/)
[![License](https://img.shields.io/badge/License-MIT-green)](#)

## 📋 Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Key Features](#key-features)
- [Demo & Screenshots](#demo--screenshots)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Model Performance](#model-performance)
- [Installation & Setup](#installation--setup)
- [Usage Guide](#usage-guide)
- [AI Features](#ai-features)
- [Dataset Information](#dataset-information)
- [Project Timeline](#project-timeline)
- [Important Considerations](#important-considerations)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## 🌟 Overview

The **EV Range Predictor** is an advanced AI-powered application that predicts electric vehicle driving ranges based on vehicle specifications. Built with machine learning and enhanced with generative AI capabilities, this platform provides comprehensive insights, recommendations, and interactive assistance for EV research and decision-making.

This project combines:
- 🤖 Machine Learning for accurate range predictions
- 🧠 AI-powered insights and recommendations
- 💬 Interactive chat assistant for EV queries
- 🎨 Professional, modern UI/UX design
- 📊 Comprehensive data analysis and visualization

## 🎯 Problem Statement

Electric Vehicles (EVs) are rapidly transforming the automotive industry, but customers still face uncertainty about real-world range and performance. This project addresses these challenges by:

- Predicting EV driving ranges based on specifications
- Providing AI-generated insights about vehicle competitiveness
- Offering maintenance tips and charging strategies
- Answering user questions through an intelligent chatbot
- Analyzing relationships between vehicle features and range

## ✨ Key Features

### 🔮 Range Prediction
- Accurate range prediction using Random Forest Regressor
- Considers model year, price, make, model, vehicle type, and location
- Achieves 99.6% R² score with minimal error

### 🤖 AI-Powered Insights
- Intelligent vehicle recommendations using DeepSeek-V3.2
- Contextual insights on vehicle competitiveness
- Real-world usage recommendations
- Automatic analysis of prediction results

### 💬 Interactive Chat Assistant
- Answer EV-related questions in real-time
- Conversational interface with chat history
- Expert-level guidance on EVs, batteries, and charging

### 🎨 Professional UI/UX
- Modern gradient-based design
- Interactive buttons with hover effects
- Color-coded result boxes and information panels
- Responsive multi-column layout
- Preset vehicle examples for quick testing

### 📊 Data Analysis & Visualization
- Comprehensive exploratory data analysis
- Distribution and correlation visualizations
- Top manufacturer analysis
- Range analysis with daily/weekly metrics

## 🖼️ Demo & Screenshots

### Main Application Interface
![EV Range Predictor Interface](https://via.placeholder.com/800x400?text=EV+Range+Predictor+Interface)

### Prediction Results with AI Insights
![Prediction Results](https://via.placeholder.com/800x400?text=Prediction+Results)

### Interactive Chat Assistant
![Chat Assistant](https://via.placeholder.com/800x400?text=Chat+Assistant)

## 📁 Project Structure

```
Electric-Vehicle/
├── .devcontainer/          # Development container configuration
├── __pycache__/            # Python cache files
├── .gitignore              # Git ignore file
├── AIapi.py                # AI Assistant module
├── Electric_Vehicle.ipynb   # Jupyter notebook with EDA and model training
├── Electric_Vehicle_Population_Data.csv  # Raw dataset
├── cleaned_ev_data.csv     # Preprocessed dataset
├── ev_range_model.joblib   # Trained ML model
├── metrics.json            # Model performance metrics
├── requirements.txt        # Python dependencies
├── streamlit_app.py        # Main Streamlit application
├── week1.md                # Week 1 documentation (EDA)
├── week2.md                # Week 2 documentation (Model Training)
└── week3.md                # Week 3 documentation (UI & AI Integration)
```

## 🛠️ Technologies Used

### Frontend & UI
- **Streamlit 1.51.0** - Web application framework
- **HTML/CSS** - Custom styling with gradients and animations

### Backend & ML
- **Python 3.8+** - Core programming language
- **pandas 2.3.3** - Data manipulation and analysis
- **scikit-learn 1.6.1** - Machine learning models
- **joblib 1.5.2** - Model serialization

### AI & NLP
- **OpenAI API (via HuggingFace)** - LLM integration
- **DeepSeek-V3.2-Exp** - State-of-the-art language model
- **python-dotenv 1.2.1** - Environment variable management

### Data Visualization
- **matplotlib** - Data plotting
- **seaborn** - Statistical visualizations
- **numpy 2.3.4** - Numerical computations

## 📊 Model Performance

Our Random Forest Regressor achieves exceptional performance:

| Metric | Value |
|--------|-------|
| **MAE (Mean Absolute Error)** | 0.873 miles |
| **RMSE (Root Mean Squared Error)** | 5.875 miles |
| **R² Score** | 0.996 (99.6%) |

**Model Features:**
- Model Year
- Base MSRP
- Make (Manufacturer)
- Model
- Electric Vehicle Type (BEV/PHEV)
- State/Location

**Hyperparameters:**
- n_estimators: 200-400
- max_depth: None, 15, 25
- Optimized using GridSearchCV with 5-fold cross-validation

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Virtual environment (recommended)
- HuggingFace API key (for AI features)

### Step 1: Clone the Repository

```bash
git clone https://github.com/chandan-911/Electric-Vehicle.git
cd Electric-Vehicle
```

### Step 2: Create Virtual Environment

```bash
# Windows
python -m venv .venv
.\.venv\Scripts\Activate

# Linux/Mac
python3 -m venv .venv
source .venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Set Up Environment Variables

Create a `.env` file in the project root:

```env
HF_TOK=your_huggingface_api_key_here
```

Or set it directly:

```bash
# Windows PowerShell
$env:HF_TOK="your_api_key_here"

# Linux/Mac
export HF_TOK="your_api_key_here"
```

### Step 5: Run the Application

```bash
streamlit run streamlit_app.py
```

The application will open in your browser at `http://localhost:8501`

## 📚 Usage Guide

### Basic Prediction Workflow

1. **Select a Preset (Optional)**
   - Choose from Tesla Model 3, Tata Nexon EV, Hyundai Kona, MG ZS EV, or Nissan Leaf
   - Or enter custom vehicle details

2. **Enter Vehicle Specifications**
   - **Basic Information:** Manufacturer, Model Year
   - **Model Details:** Model Name, Vehicle Type (BEV/PHEV)
   - **Pricing & Location:** Base MSRP, State

3. **Click Predict Range**
   - View predicted driving range
   - Get AI-generated insights
   - See detailed range analysis

4. **Explore AI Features**
   - Read AI insights about your vehicle
   - Ask questions in the chat assistant
   - Get maintenance tips and charging strategies

### Example Input

```
Make: Tesla
Model: Model 3
Year: 2023
Type: BEV
MSRP: $46,990
State: CA

✅ Predicted Range: 358.5 miles
```

## 🤖 AI Features

The application includes a comprehensive `EVAIAssistant` class with multiple AI capabilities:

### 1. Vehicle Recommendations
- Analyzes specifications and predicted range
- Provides professional insights on competitiveness
- Recommends best use cases

### 2. Maintenance Tips
- Battery health management strategies
- Seasonal care recommendations
- Charging best practices

### 3. Charging Strategy
- Optimal charging frequency based on usage
- Home vs. public charging recommendations
- Cost-effective charging times

### 4. General Q&A
- Answer EV-related questions
- Expert guidance on batteries and technology
- Sustainability and cost-of-ownership info

### 5. Vehicle Comparison
- Side-by-side vehicle analysis
- Feature and price comparisons
- Use-case recommendations

## 📊 Dataset Information

**Source:** Electric Vehicle Population Data

**Size:** 177,866 records × 17 features

**Key Features:**
- VIN (1-10)
- County, City, State
- Postal Code
- Model Year (1997-2024)
- Make (40 manufacturers)
- Model (139 different models)
- Electric Vehicle Type (BEV/PHEV)
- Electric Range (0-337 miles)
- Base MSRP
- Legislative District
- DOL Vehicle ID
- Vehicle Location
- Electric Utility
- 2020 Census Tract

**Data Cleaning:**
- Handled missing values using median/mode imputation
- Removed duplicates
- Cleaned categorical columns
- Standardized manufacturer and model names

## 📅 Project Timeline

### Week 1: Exploratory Data Analysis
- ✅ Data loading and exploration
- ✅ Missing value analysis
- ✅ Data cleaning and preprocessing
- ✅ Statistical analysis and visualizations
- ✅ Correlation heatmap generation
- ✅ Distribution analysis

### Week 2: Model Training & Deployment
- ✅ Feature engineering
- ✅ Train/test split
- ✅ Model selection (Random Forest)
- ✅ Hyperparameter tuning with GridSearchCV
- ✅ Model evaluation (MAE: 0.873, R²: 0.996)
- ✅ Model serialization
- ✅ Streamlit app development

### Week 3: UI Enhancement & AI Integration
- ✅ Professional UI/UX design with gradients
- ✅ AI API integration (DeepSeek-V3.2)
- ✅ Interactive chat assistant
- ✅ AI-powered insights generation
- ✅ Preset vehicle examples
- ✅ Comprehensive documentation

## ⚠️ Important Considerations

### Range Prediction Accuracy

The predicted range can vary by ±15-25% based on:

- **❄️ Temperature:** Cold weather reduces range by 20-40%
- **🏎️ Driving Style:** Aggressive acceleration decreases efficiency
- **🛣️ Terrain:** Highways vs. city driving efficiency differences
- **🌡️ Accessories:** HVAC systems impact consumption
- **🔋 Battery Age:** Degradation occurs over charging cycles
- **🌬️ Road Conditions:** Traffic, wind, and elevation affect consumption

### Recommendations

- Plan long trips with charging stations in mind
- Precondition battery before departure in cold weather
- Monitor battery health regularly
- Use eco-driving modes for maximum range
- Refer to manufacturer specifications for accurate estimates

### AI Response Reliability

- AI provides informed recommendations, not guarantees
- Always verify against official manufacturer specifications
- Use AI insights as advisory guidance
- Consult experts for technical decisions

## 🚀 Future Enhancements

### Planned Features

- [ ] Historical range data and trends analysis
- [ ] User profiles with saved vehicle configurations
- [ ] Real-time market price comparisons
- [ ] Charging network integration with nearby stations
- [ ] Carbon footprint calculations
- [ ] Multiple language support
- [ ] Mobile app optimization
- [ ] PDF report generation
- [ ] Vehicle comparison tool
- [ ] Real-time battery health monitoring
- [ ] Integration with OBD-II devices
- [ ] Weather-adjusted range predictions

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines

- Follow PEP 8 style guidelines
- Add unit tests for new features
- Update documentation
- Test thoroughly before submitting PR

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Chandan**
- GitHub: [@chandan-911](https://github.com/chandan-911)
- Project Link: [https://github.com/chandan-911/Electric-Vehicle](https://github.com/chandan-911/Electric-Vehicle)

## 🙏 Acknowledgments

- Electric Vehicle Population dataset providers
- HuggingFace for AI API infrastructure
- Streamlit team for the amazing framework
- scikit-learn community for ML tools
- DeepSeek AI for the powerful language model

## 📞 Support

If you have any questions or issues, please:
- Open an issue on GitHub
- Check the [week1.md](week1.md), [week2.md](week2.md), and [week3.md](week3.md) documentation
- Review the troubleshooting section in [week3.md](week3.md)

---

<div align="center">

**Made with ❤️ by Chandan**

⭐ Star this repository if you find it helpful!

[Report Bug](https://github.com/chandan-911/Electric-Vehicle/issues) · [Request Feature](https://github.com/chandan-911/Electric-Vehicle/issues)

</div>
