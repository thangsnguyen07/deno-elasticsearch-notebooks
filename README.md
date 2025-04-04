# Elasticsearch with Deno and Jupyter Notebooks

This project provides examples and tutorials on how to use Elasticsearch with Deno and Jupyter Notebooks. The project includes practical examples of interacting with Elasticsearch, performing search queries, and data analysis.

## Project Structure

```
.
├── data/                  # Sample data directory
├── elastic-start-local/   # Local Elasticsearch configuration and startup scripts
├── images/               # Images and resources
├── notebooks/            # Jupyter notebooks with examples
├── deno.json            # Deno configuration
├── deno.lock            # Deno lock file
├── main.ts              # Main application file
└── main_test.ts         # Test file
```

## Requirements

- [Deno](https://deno.land/) (latest version)
- [Elasticsearch](https://www.elastic.co/elasticsearch/) (version 8.x)
- [Jupyter Notebook](https://jupyter.org/)
- [VS Code](https://code.visualstudio.com/)

## Installation and Setup

### 1. Install Deno

```bash
# Windows (PowerShell)
irm https://deno.land/install.ps1 | iex

# Linux/macOS
curl -fsSL https://deno.land/x/install/install.sh | sh
```

Verify installation:

```bash
deno --version
```

### 2. Install Deno Kernel

```bash
deno jupyter --unstable --install
```

### 3. VS Code Setup

Install the "Jupyter" extension for VS Code

- Open VS Code
- Go to Extensions (Ctrl+Shift+X)
- Search for "Jupyter"
- Install the official Jupyter extension by Microsoft

### 4. Clone and Setup Project

```bash
# Clone repository
git clone https://github.com/thangsnguyen07/deno-elasticsearch-notebooks.git
cd deno-elasticsearch-notebooks

# Install dependencies
deno cache main.ts
```

### 5. Start Local Elasticsearch

```bash
curl -fsSL https://elastic.co/start-local | sh
```

After running the command, you'll see output similar to this:

```
🎉 Congrats, Elasticsearch and Kibana are installed and running in Docker!

🌐 Open your browser at http://localhost:5601

   Username: elastic
   Password: [your-password]

🔌 Elasticsearch API endpoint: http://localhost:9200
🔑 API key: [your-api-key]
```

Save the API key and password as they will be needed for authentication in the notebooks.

### 6. Configure Elasticsearch Connection

Create a `.env` file in the root directory:

```bash
ELASTICSEARCH_API_KEY=[your-api-key]
ELASTICSEARCH_NODE=http://localhost:9200
```

## Usage

### Working with Jupyter Notebooks

1. Open VS Code
2. Open any `.ipynb` file from the `notebooks/` directory
3. Click on the kernel selector in the top right corner
4. Select "Deno" as your kernel
5. Start coding!

The notebooks provide detailed examples of:

- Connecting to Elasticsearch
- Performing basic search queries
- Data analysis with Elasticsearch
- Visualization and reporting

## Troubleshooting

### Common Issues

1. **Deno Kernel Not Found**

   - Ensure Deno is in your PATH
   - Try reinstalling the Deno kernel
   - Check VS Code Jupyter extension settings

2. **Elasticsearch Connection Issues**
   - Verify Elasticsearch is running
   - Check the connection settings in your notebooks
   - Ensure proper permissions are set

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue to discuss proposed changes.

## License

MIT License
