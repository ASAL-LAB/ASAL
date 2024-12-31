<h1 align="center">
  <img width="600" alt="ASAL - Accelerating Artificial Life" src="assets/cover.png"><br>
</h1>

<h1 align="center">
ASAL: Advanced Simulation of Artificial Life
</h1>

<p align="center">
  🧬 <a href="https://github.com/AsalLabs-eng/ASAL-Models-Deploy">[Project]</a> |
  📚 <a href="https://x.com/asalsolana">[Documentation]</a>
</p>

## About ASAL

ASAL represents a breakthrough in artificial life research, leveraging advanced foundation models to accelerate the discovery and optimization of complex emergent systems. Our framework enables automated exploration of artificial life phenomena through sophisticated simulation and analysis techniques.

## Key Features

- Intelligent parameter space exploration via foundation models
- High-performance simulation engine powered by JAX
- Extensive library of artificial life substrates
- Advanced optimization and analysis tools

## Supported Simulation Models

ASAL provides a comprehensive suite of artificial life models:

- Lenia
- Boids
- Particle Life
- Particle Life++
- Particle Lenia  
- Discrete Neural Cellular Automata
- Continuous Neural Cellular Automata
- Game of Life/Life-Like Cellular Automata

Each model is carefully implemented and optimized for performance. See [models/](models/) for implementation details.

## Main Components

The main files to run ASAL are:
- `main_opt.py` - Advanced optimization engine for targeted evolution
- `main_illuminate.py` - Novel illumination algorithms for pattern discovery  
- `main_sweep_gol.py` - Systematic exploration of cellular automata dynamics

## Installation

```sh
git clone https://github.com/AsalLabs-eng/ASAL-Models-Deploy.git
cd ASAL-Models-Deploy

# Create conda environment
conda create --name asal python=3.10.13
conda activate asal

# Install dependencies
pip install -r requirements.txt
```

For GPU acceleration, please [manually install JAX](https://github.com/google/jax#installation) according to your system's CUDA version.

## Deployment

### Local Development
```sh
# Run simulation locally
python main_opt.py --sim boids --save_dir results
```

### Cloud Deployment
For large-scale experiments, we recommend deploying on GPU-enabled cloud infrastructure:

1. **Cloud Setup**
```sh
# Install on cloud instance
git clone https://github.com/AsalLabs-eng/ASAL-Models-Deploy.git
cd ASAL-Models-Deploy
./scripts/setup_cloud.sh
```

2. **Docker Deployment**
```sh
# Build Docker image
docker build -t asal .

# Run container
docker run -it --gpus all asal
```

3. **Kubernetes Deployment**
```sh
# Deploy to k8s cluster
kubectl apply -f k8s/deployment.yaml
```

### Monitoring
- Use Prometheus + Grafana for metrics
- Monitor GPU utilization and simulation progress
- Track optimization convergence

### Production Tips
- Use environment variables for configuration
- Enable logging for debugging
- Set up automated backups
- Configure proper security measures

## Future Development

Our roadmap includes:
- Enhanced pattern discovery algorithms
- Advanced visualization tools
- Distributed computation support
- Extended model library

## Contributing

We welcome contributions! Please see our [contributing guidelines](CONTRIBUTING.md) for details.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Team

ASAL is developed by a dedicated team of researchers and engineers at the intersection of artificial life and machine learning.

## Citation

```bibtex
@article{asal2024,
  title={ASAL: Advanced Simulation of Artificial Life},
  author={Power by Sakana.ai},
  year={2024},
  url={https://github.com/AsalLabs-eng/ASAL-Models-Deploy}
}
```


