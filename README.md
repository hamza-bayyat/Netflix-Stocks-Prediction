# Netflix-stock-prediction
A comparative study predicting the stock market is famously difficult, but deep learning offers powerful tools to capture the hidden patterns in temporal data. This project explores the effectiveness of three different neural network architectures—ESN, LSTM, and Bi-LSTM—in forecasting Netflix ($NFLX$) stock prices using a decade of historical data.

📊 Dataset Overview: The dataset contains Netflix stock prices spanning from 2014 to 2023. To provide the models with more context than just raw prices, several technical indicators were calculated and included:
Core Columns: Date, Open, High, Low, Close, Volume.
Technical Indicators: RSI (7 and 14 days), CCI (7 and 14 days), and more.

🛠️ Methodology & Preprocessing: To ensure the models could learn effectively, the data underwent rigorous preparation:
Indexing: Data was indexed by date to maintain chronological order for time series modeling.
Scaling: MinMaxScaler was applied to all features to improve model convergence and stability.
Sequencing: Stock price data was converted into overlapping sequences to prepare the input for LSTM-based architectures.

🧠 Model Architectures:
implemented three distinct models to compare their strengths:
Echo State Network (ESN): Utilized for reservoir computing; while it captured basic dependencies, it struggled with the longer sequences inherent in stock data.
Long Short-Term Memory (LSTM): A sequential model that significantly improved results by retaining long-term dependencies through its gating mechanisms.
Bi-Directional LSTM (Bi-LSTM): The top-performing model, which extended the LSTM architecture to understand both past and future context within the sequences.

💻 Tech Stack
Framework: TensorFlow / Keras 
Libraries: NumPy, Matplotlib, Scikit-learn 
Hardware: Local GPU-enabled system for accelerated training
