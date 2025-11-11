# Supply Chain Libraries & Tools

Curated collection of libraries, frameworks, and tools for supply chain development and analysis.

## Table of Contents

- [Python Libraries](#python-libraries)
- [R Packages](#r-packages)
- [JavaScript/TypeScript](#javascripttypescript)
- [Java Libraries](#java-libraries)
- [Data & Analytics Platforms](#data--analytics-platforms)
- [Commercial Software SDKs](#commercial-software-sdks)

## Python Libraries

### Supply Chain Specific

#### supplychainpy

**Description**: Python library for supply chain analysis, modeling and simulation
- **GitHub**: https://github.com/KevinFasusi/supplychainpy
- **Features**:
  - Inventory analysis and optimization
  - Demand forecasting
  - Inventory profiling (ABC/XYZ analysis)
  - Economic order quantity (EOQ) calculations
  - Reorder point analysis
  - Safety stock calculations
  - Simulation capabilities

**Installation**:
```bash
pip install supplychainpy
```

**Use Cases**:
- Inventory management analysis
- Demand planning
- Supply chain simulation
- Reporting and visualization

### Optimization

#### PuLP

**Description**: Linear programming modeler written in Python
- **GitHub**: https://github.com/coin-or/pulp
- **Documentation**: https://coin-or.github.io/pulp/
- **Solvers**: CBC (default), GLPK, CPLEX, Gurobi

**Installation**:
```bash
pip install pulp
```

**Example**:
```python
from pulp import *

# Define problem
prob = LpProblem("Supply_Chain", LpMinimize)

# Define variables
x = LpVariable("x", lowBound=0)
y = LpVariable("y", lowBound=0)

# Objective function
prob += 2*x + 3*y

# Constraints
prob += x + y >= 5
prob += 2*x + y >= 8

# Solve
prob.solve()
print(f"Status: {LpStatus[prob.status]}")
print(f"Optimal value: {value(prob.objective)}")
```

#### Pyomo

**Description**: Python-based optimization modeling language
- **GitHub**: https://github.com/Pyomo/pyomo
- **Documentation**: https://pyomo.readthedocs.io/
- **Features**:
  - Algebraic modeling language
  - Supports LP, MIP, NLP, MINLP
  - Integration with multiple solvers
  - Stochastic programming
  - Robust optimization

**Installation**:
```bash
pip install pyomo
```

**Use Cases**:
- Production planning
- Network design
- Facility location
- Transportation optimization
- Inventory optimization

#### Google OR-Tools

**Description**: Google's optimization tools
- **GitHub**: https://github.com/google/or-tools
- **Documentation**: https://developers.google.com/optimization
- **Capabilities**:
  - Constraint programming
  - Linear and mixed-integer programming
  - Vehicle routing
  - Graph algorithms
  - Assignment problems

**Installation**:
```bash
pip install ortools
```

**Key Modules**:
- `pywraplp`: Linear programming
- `pywrapcp`: Constraint programming
- `routing`: Vehicle routing problems
- `sat`: SAT solver

**Example (VRP)**:
```python
from ortools.constraint_solver import routing_enums_pb2
from ortools.constraint_solver import pywrapcp

# Define routing problem
manager = pywrapcp.RoutingIndexManager(len(distance_matrix), num_vehicles, depot)
routing = pywrapcp.RoutingModel(manager)

# Define cost callback
def distance_callback(from_index, to_index):
    from_node = manager.IndexToNode(from_index)
    to_node = manager.IndexToNode(to_index)
    return distance_matrix[from_node][to_node]

transit_callback_index = routing.RegisterTransitCallback(distance_callback)
routing.SetArcCostEvaluatorOfAllVehicles(transit_callback_index)

# Solve
solution = routing.SolveWithParameters(search_parameters)
```

#### CVXPY

**Description**: Convex optimization library
- **GitHub**: https://github.com/cvxpy/cvxpy
- **Documentation**: https://www.cvxpy.org/
- **Focus**: Convex optimization problems

**Installation**:
```bash
pip install cvxpy
```

### Forecasting & Time Series

#### Prophet

**Description**: Facebook's time series forecasting tool
- **GitHub**: https://github.com/facebook/prophet
- **Documentation**: https://facebook.github.io/prophet/
- **Features**:
  - Automatic seasonality detection
  - Holiday effects
  - Trend changepoints
  - Robust to missing data

**Installation**:
```bash
pip install prophet
```

**Example**:
```python
from prophet import Prophet
import pandas as pd

# Prepare data
df = pd.DataFrame({'ds': dates, 'y': values})

# Fit model
model = Prophet(yearly_seasonality=True, weekly_seasonality=True)
model.fit(df)

# Make predictions
future = model.make_future_dataframe(periods=30)
forecast = model.predict(future)
```

#### statsmodels

**Description**: Statistical modeling and econometrics
- **GitHub**: https://github.com/statsmodels/statsmodels
- **Documentation**: https://www.statsmodels.org/
- **Capabilities**:
  - ARIMA, SARIMA
  - Exponential smoothing
  - VAR models
  - Statistical tests

**Installation**:
```bash
pip install statsmodels
```

#### Darts

**Description**: Time series forecasting library
- **GitHub**: https://github.com/unit8co/darts
- **Documentation**: https://unit8co.github.io/darts/
- **Models**:
  - Statistical (ARIMA, Exponential Smoothing)
  - Machine learning (Random Forest, LightGBM)
  - Deep learning (LSTM, Transformer, N-BEATS)
  - Ensemble methods

**Installation**:
```bash
pip install darts
```

#### GluonTS

**Description**: Deep learning toolkit for time series by AWS
- **GitHub**: https://github.com/awslabs/gluonts
- **Documentation**: https://ts.gluon.ai/
- **Models**: DeepAR, Transformer, N-BEATS, WaveNet

**Installation**:
```bash
pip install gluonts
```

#### Chronos (Amazon) ⭐ NEW 2024-2025

**Description**: Foundation models for time series forecasting
- **GitHub**: https://github.com/amazon-science/chronos-forecasting
- **Key Features**:
  - Zero-shot forecasting capabilities
  - Pre-trained on diverse time series data
  - Based on T5 transformer architecture
  - **Chronos-Bolt** (Nov 2024): 5% lower error, 250x faster, 20x more memory efficient
  - **Chronos-2** (2025): Multivariate and covariate-informed forecasting
  - Available on Amazon SageMaker JumpStart (Feb 2025)

**Installation**:
```bash
pip install chronos-forecasting
```

**Example**:
```python
from chronos import ChronosPipeline
import torch

# Load pre-trained model
pipeline = ChronosPipeline.from_pretrained(
    "amazon/chronos-t5-small",
    device_map="cuda",
    torch_dtype=torch.bfloat16,
)

# Zero-shot forecast
forecast = pipeline.predict(
    context=historical_data,
    prediction_length=12
)
```

#### Nixtla TimeGPT ⭐ NEW 2024-2025

**Description**: First foundation model for time series forecasting
- **GitHub**: https://github.com/Nixtla/nixtla
- **Website**: https://www.nixtla.io/
- **Key Features**:
  - Trained on 100B+ data points from finance, weather, energy, web data
  - Production-ready generative pre-trained transformer
  - Zero-shot forecasting and anomaly detection
  - Handles retail, electricity, finance, IoT domains
  - Available via API or self-hosted

**Installation**:
```bash
pip install nixtla
```

**Example**:
```python
from nixtla import NixtlaClient

# Initialize client
nixtla_client = NixtlaClient(api_key='your_api_key')

# Forecast
forecast = nixtla_client.forecast(
    df=df,
    h=12,
    time_col='timestamp',
    target_col='value'
)
```

#### NeuralForecast (Nixtla) ⭐ NEW 2024-2025

**Description**: Deep learning time series forecasting library
- **GitHub**: https://github.com/Nixtla/neuralforecast
- **PyPI**: https://pypi.org/project/neuralforecast/ (Latest: v3.1.2, Oct 2025)
- **Models**:
  - LSTM, GRU, RNN variants
  - N-BEATS, N-HiTS
  - Transformers (TFT, Informer, Autoformer)
  - MLP-based models
  - Ensemble methods

**Installation**:
```bash
pip install neuralforecast
```

**Example**:
```python
from neuralforecast import NeuralForecast
from neuralforecast.models import NBEATS, NHITS
from neuralforecast.utils import AirPassengersDF

# Define models
models = [NBEATS(input_size=24, h=12, max_steps=100),
          NHITS(input_size=24, h=12, max_steps=100)]

# Fit and predict
nf = NeuralForecast(models=models, freq='M')
nf.fit(df=AirPassengersDF)
forecasts = nf.predict()
```

#### StatsForecast (Nixtla) ⭐ NEW 2024-2025

**Description**: Lightning-fast statistical forecasting
- **GitHub**: https://github.com/Nixtla/statsforecast
- **Key Features**:
  - First library to efficiently forecast millions of time series
  - Optimized AutoARIMA implementation
  - 10x-100x faster than traditional implementations
  - Includes ETS, Theta, CES, and more

**Installation**:
```bash
pip install statsforecast
```

**Example**:
```python
from statsforecast import StatsForecast
from statsforecast.models import AutoARIMA, AutoETS

# Define models
models = [AutoARIMA(season_length=12),
          AutoETS(season_length=12)]

# Fit and forecast
sf = StatsForecast(models=models, freq='M', n_jobs=-1)
forecasts = sf.forecast(h=12)
```

### Reinforcement Learning ⭐ NEW 2024-2025

#### Stable-Baselines3

**Description**: Reliable implementations of RL algorithms
- **GitHub**: https://github.com/DLR-RM/stable-baselines3
- **Documentation**: https://stable-baselines3.readthedocs.io/
- **Algorithms**: PPO, A2C, SAC, TD3, DQN
- **Use Cases**:
  - Inventory management policies
  - Dynamic pricing
  - Route optimization
  - Production scheduling

**Installation**:
```bash
pip install stable-baselines3
```

**Example**:
```python
from stable_baselines3 import PPO
import gym

# Create environment
env = gym.make('InventoryManagement-v0')

# Train agent
model = PPO('MlpPolicy', env, verbose=1)
model.learn(total_timesteps=100000)

# Use trained policy
obs = env.reset()
action, _states = model.predict(obs)
```

#### Ray RLlib

**Description**: Scalable reinforcement learning library
- **GitHub**: https://github.com/ray-project/ray
- **Documentation**: https://docs.ray.io/en/latest/rllib/
- **Features**:
  - Multi-agent RL support
  - Distributed training
  - Production deployment
  - Integration with major frameworks

**Installation**:
```bash
pip install ray[rllib]
```

**Use Cases for Supply Chain**:
- Multi-agent inventory optimization
- Distributed warehouse control
- Fleet coordination
- Supply network optimization

### Machine Learning

#### scikit-learn

**Description**: Machine learning library
- **GitHub**: https://github.com/scikit-learn/scikit-learn
- **Documentation**: https://scikit-learn.org/
- **Algorithms**:
  - Regression (Linear, Ridge, Lasso)
  - Classification (SVM, Random Forest)
  - Clustering (K-means, DBSCAN)
  - Ensemble methods (Gradient Boosting)

**Installation**:
```bash
pip install scikit-learn
```

#### XGBoost / LightGBM / CatBoost

**Description**: Gradient boosting frameworks
- **XGBoost**: https://github.com/dmlc/xgboost
- **LightGBM**: https://github.com/microsoft/LightGBM
- **CatBoost**: https://github.com/catboost/catboost

**Use Cases**:
- Demand forecasting
- Classification problems
- Feature importance analysis

**Installation**:
```bash
pip install xgboost lightgbm catboost
```

#### TensorFlow / Keras

**Description**: Deep learning framework by Google
- **GitHub**: https://github.com/tensorflow/tensorflow
- **Documentation**: https://www.tensorflow.org/
- **Applications**:
  - Neural networks for forecasting
  - Computer vision for quality control
  - Reinforcement learning for optimization

**Installation**:
```bash
pip install tensorflow
```

#### PyTorch

**Description**: Deep learning framework by Meta
- **GitHub**: https://github.com/pytorch/pytorch
- **Documentation**: https://pytorch.org/
- **Features**:
  - Dynamic computational graphs
  - Research-friendly
  - Production deployment (TorchServe)

**Installation**:
```bash
pip install torch
```

### Simulation

#### SimPy

**Description**: Discrete-event simulation framework
- **GitLab**: https://gitlab.com/team-simpy/simpy
- **Documentation**: https://simpy.readthedocs.io/
- **Use Cases**:
  - Warehouse simulation
  - Production line modeling
  - Queue analysis
  - Resource allocation

**Installation**:
```bash
pip install simpy
```

**Example**:
```python
import simpy

def warehouse_process(env, name):
    print(f'{name} arriving at {env.now}')
    yield env.timeout(5)  # Processing time
    print(f'{name} departing at {env.now}')

env = simpy.Environment()
env.process(warehouse_process(env, 'Order 1'))
env.run(until=10)
```

#### Mesa

**Description**: Agent-based modeling framework
- **GitHub**: https://github.com/projectmesa/mesa
- **Documentation**: https://mesa.readthedocs.io/
- **Use Cases**: Supply chain dynamics, market behavior

**Installation**:
```bash
pip install mesa
```

### Network Analysis

#### NetworkX

**Description**: Network analysis library
- **GitHub**: https://github.com/networkx/networkx
- **Documentation**: https://networkx.org/
- **Algorithms**:
  - Shortest path
  - Network flow
  - Centrality measures
  - Community detection

**Installation**:
```bash
pip install networkx
```

**Use Cases**:
- Supply chain network design
- Transportation network optimization
- Supplier relationship analysis

### Data Processing

#### Pandas

**Description**: Data manipulation and analysis
- **GitHub**: https://github.com/pandas-dev/pandas
- **Documentation**: https://pandas.pydata.org/

**Installation**:
```bash
pip install pandas
```

#### Polars

**Description**: Fast DataFrame library (Rust-based)
- **GitHub**: https://github.com/pola-rs/polars
- **Documentation**: https://pola-rs.github.io/polars/
- **Benefits**: 10-100x faster than Pandas for large datasets

**Installation**:
```bash
pip install polars
```

#### NumPy

**Description**: Numerical computing
- **GitHub**: https://github.com/numpy/numpy
- **Documentation**: https://numpy.org/

**Installation**:
```bash
pip install numpy
```

### Visualization

#### Matplotlib

**Description**: Plotting library
- **GitHub**: https://github.com/matplotlib/matplotlib
- **Documentation**: https://matplotlib.org/

**Installation**:
```bash
pip install matplotlib
```

#### Plotly

**Description**: Interactive visualization
- **GitHub**: https://github.com/plotly/plotly.py
- **Documentation**: https://plotly.com/python/

**Installation**:
```bash
pip install plotly
```

#### Seaborn

**Description**: Statistical visualization
- **GitHub**: https://github.com/mwaskom/seaborn
- **Documentation**: https://seaborn.pydata.org/

**Installation**:
```bash
pip install seaborn
```

## R Packages

### Forecasting

#### forecast

**Description**: Forecasting functions for time series
- **CRAN**: https://cran.r-project.org/package=forecast
- **GitHub**: https://github.com/robjhyndman/forecast
- **Functions**: auto.arima(), ets(), stlf(), tbats()

**Installation**:
```r
install.packages("forecast")
```

#### prophet

**Description**: R interface to Facebook Prophet
- **CRAN**: https://cran.r-project.org/package=prophet

**Installation**:
```r
install.packages("prophet")
```

### Optimization

#### lpSolve

**Description**: Linear and integer programming
- **CRAN**: https://cran.r-project.org/package=lpSolve

**Installation**:
```r
install.packages("lpSolve")
```

#### ompr

**Description**: Optimization modeling in R
- **GitHub**: https://github.com/dirkschumacher/ompr
- **CRAN**: https://cran.r-project.org/package=ompr

**Installation**:
```r
install.packages("ompr")
```

### Supply Chain

#### SCperf

**Description**: Supply chain performance measurement
- **CRAN**: https://cran.r-project.org/package=SCperf

**Installation**:
```r
install.packages("SCperf")
```

## JavaScript/TypeScript

### Optimization

#### jsLPSolver

**Description**: Linear programming in JavaScript
- **GitHub**: https://github.com/JWally/jsLPSolver
- **npm**: https://www.npmjs.com/package/javascript-lp-solver

**Installation**:
```bash
npm install javascript-lp-solver
```

### Visualization

#### D3.js

**Description**: Data visualization library
- **GitHub**: https://github.com/d3/d3
- **Website**: https://d3js.org/

**Installation**:
```bash
npm install d3
```

#### Chart.js

**Description**: Simple charting library
- **GitHub**: https://github.com/chartjs/Chart.js
- **Website**: https://www.chartjs.org/

**Installation**:
```bash
npm install chart.js
```

## Java Libraries

### OptaPlanner

**Description**: Constraint satisfaction solver
- **GitHub**: https://github.com/kiegroup/optaplanner
- **Website**: https://www.optaplanner.org/
- **Use Cases**:
  - Vehicle routing
  - Employee rostering
  - Task assignment
  - Production scheduling

**Maven**:
```xml
<dependency>
    <groupId>org.optaplanner</groupId>
    <artifactId>optaplanner-core</artifactId>
</dependency>
```

### jsprit

**Description**: Vehicle routing problem solver
- **GitHub**: https://github.com/graphhopper/jsprit
- **Features**:
  - Multiple VRP variants
  - Time windows
  - Pickup and delivery
  - Multi-depot

## Data & Analytics Platforms

### Apache Spark

**Description**: Big data processing engine
- **Website**: https://spark.apache.org/
- **Python Interface**: PySpark
- **Use Cases**:
  - Large-scale data processing
  - Machine learning (MLlib)
  - Stream processing

**Installation**:
```bash
pip install pyspark
```

### Apache Kafka

**Description**: Distributed streaming platform
- **Website**: https://kafka.apache.org/
- **Use Cases**:
  - Real-time data pipelines
  - Event streaming
  - IoT data ingestion

### Dask

**Description**: Parallel computing in Python
- **GitHub**: https://github.com/dask/dask
- **Website**: https://www.dask.org/
- **Features**: Scales Pandas and NumPy to larger-than-memory datasets

**Installation**:
```bash
pip install dask
```

## Commercial Software SDKs

### AWS

- **boto3**: Python SDK for AWS services
- **SageMaker**: ML platform
- **S3**: Object storage
- **Athena**: SQL queries on S3

### Azure

- **azure-sdk-for-python**: Python SDK
- **Azure ML**: Machine learning
- **Azure IoT**: IoT solutions

### Google Cloud

- **google-cloud-python**: Python SDK
- **BigQuery**: Data warehouse
- **Vertex AI**: ML platform

## Development Tools

### Version Control
- **Git**: https://git-scm.com/
- **GitHub/GitLab/Bitbucket**: Code hosting

### IDEs & Editors
- **VS Code**: https://code.visualstudio.com/
- **PyCharm**: https://www.jetbrains.com/pycharm/
- **Jupyter Notebook**: https://jupyter.org/
- **JupyterLab**: Next-generation Jupyter

### Package Management
- **pip**: Python package installer
- **conda**: Cross-platform package manager
- **poetry**: Python dependency management

### Testing
- **pytest**: Python testing framework
- **unittest**: Built-in Python testing
- **coverage**: Code coverage measurement

## Learning Resources

### Documentation
- Each library's official documentation
- Stack Overflow for Q&A
- GitHub issues and discussions

### Tutorials
- Kaggle Learn courses
- DataCamp
- Coursera and edX
- YouTube tutorials

### Books
- "Python for Data Analysis" by Wes McKinney
- "Forecasting: Principles and Practice" by Hyndman & Athanasopoulos (free online)
- "Introduction to Operations Research" by Hillier & Lieberman
- "Deep Learning" by Goodfellow, Bengio, and Courville

---

**Last Updated**: November 2025
