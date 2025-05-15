# Social Network Analysis Project

## Overview
This project conducts a comprehensive analysis of social network data from the Stanford Network Analysis Project (SNAP). The analysis includes exploratory network statistics, robustness testing, community detection, and simulations of opinion dynamics and information spread.

## Dataset
- **Source:** Stanford Network Analysis Project (SNAP)
- **Format:** Edge list file (0.edges)
- **Size:** 3959 nodes, 84243 edges
- **Type:** Undirected and unweighted network
- **Average Degree:** 42.56
- **Density:** 0.0108

## Features
1. **Network Preprocessing**
   - Removal of self-loops and duplicate edges
   - Graph construction using NetworkX

2. **Exploratory Analysis**
   - Degree distribution analysis
   - Centrality measures (Degree and Betweenness)
   - Connected component analysis

3. **Robustness Testing**
   - Random node failure simulation
   - Targeted attack simulation (by node degree)
   - Comparative resilience analysis

4. **Community Detection**
   - Greedy modularity optimization method
   - Community visualization and analysis

5. **Dynamic Processes**
   - Voter Model for opinion dynamics
   - SIR Model for information/epidemic spread (Beta=0.03, Gamma=0.01)

## Key Findings
- The network demonstrates significant resilience to random failures but high vulnerability to targeted attacks
- Well-defined community structure identified through modularity optimization
- Simulations reveal interesting patterns in both opinion consensus formation and information diffusion
- Results have potential applications in public health, information spread analysis, and community-based system design

## Requirements
- Python 3.8+
- NetworkX
- Matplotlib
- NumPy
- Pandas
- SciPy

## Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/social-network-analysis.git
cd social-network-analysis

# Create and activate virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Usage
1. **Data Preprocessing**
   ```python
   from src.preprocessing import clean_network_data
   
   G = clean_network_data('data/0.edges')
   ```

2. **Run Network Analysis**
   ```python
   from src.network_metrics import calculate_centralities
   
   centrality_scores = calculate_centralities(G)
   ```

3. **Run Simulations**
   ```python
   from src.simulation import run_sir_model
   
   results = run_sir_model(G, beta=0.03, gamma=0.01, steps=100)
   ```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
[MIT License](LICENSE)

## Acknowledgments
- Stanford Network Analysis Project (SNAP) for providing the dataset
- NetworkX development team for their comprehensive network analysis library
