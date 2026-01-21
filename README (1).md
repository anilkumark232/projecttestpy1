# BB84 Quantum Key Distribution Simulator

An interactive web-based simulator for the BB84 quantum key distribution protocol, built with Streamlit and deployed using stlite on GitHub Pages.

## 🚀 Live Demo

Once deployed, your app will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

## 📋 Features

- **Interactive Simulation**: Configure parameters and run BB84 protocol simulations in real-time
- **Visual Timeline**: Detailed visualization of bit transmission, basis matching, and errors
- **Scenario Comparison**: Compare secure transmission (no eavesdropper) vs. compromised transmission (with Eve)
- **Educational**: Learn about quantum cryptography with built-in explanations
- **No Server Required**: Runs entirely in your browser using WebAssembly (Pyodide)

## 🛠️ Technology Stack

- **Streamlit**: Web application framework
- **stlite**: Serverless Streamlit using WebAssembly
- **Qiskit**: Quantum computing framework for BB84 simulation
- **NumPy & Pandas**: Data processing
- **Matplotlib**: Visualization
- **GitHub Pages**: Static hosting

## 📦 Deployment Instructions

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it something like `bb84-simulator`
3. Make it public (required for GitHub Pages)
4. Don't initialize with README (we'll add files)

### Step 2: Upload Files

1. Clone your repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
   ```

2. Copy the `index.html` file to your repository root

3. Commit and push:
   ```bash
   git add index.html
   git commit -m "Initial commit: BB84 simulator"
   git push origin main
   ```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** (top navigation)
3. Click on **Pages** (left sidebar)
4. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes for deployment
7. Your app will be live at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

### Step 4: Configure GitHub Pages URL (Optional)

1. Go back to your repository main page
2. Click the gear icon ⚙️ next to "About"
3. Check "Use your GitHub Pages website"
4. Add a description and topics
5. Click "Save changes"

## 🎯 Usage

1. **Open the app** in your browser
2. **Configure parameters** in the left sidebar:
   - Number of bits to transmit (50-500)
   - QBER threshold (0.05-0.20)
   - Random seed for reproducibility
   - Maximum display bits for visualization
3. **Select scenario**:
   - No Eavesdropper: Secure transmission
   - With Eavesdropper: Eve intercepts with configurable probability
   - Compare Both: Side-by-side comparison
4. **Click "Run Simulation"** to execute
5. **Explore results**:
   - View metrics (transmitted bits, QBER, final key length)
   - Analyze timeline visualizations
   - Examine detailed data tables
   - Compare scenarios

## 📊 Understanding the Visualizations

### Alice's Transmitted Bits
- **Cyan bars** (height 0.2): Represents 0-bits
- **Navy bars** (height 1.0): Represents 1-bits
- Shows the original quantum states Alice prepares

### Base Matching
- **Lime green**: Matching bases (bits kept after sifting)
- **Crimson**: Mismatched bases (bits discarded)

### Transmission Results
- **Forest green**: Correct transmission (no error)
- **Red**: Transmission error detected
- **Light gray**: Bit not used (basis mismatch)

## 🔐 About BB84 Protocol

The BB84 protocol, invented by Charles Bennett and Gilles Brassard in 1984, is the first quantum cryptography protocol. It uses quantum mechanics principles to:

- Enable secure key distribution between two parties
- Detect eavesdropping through quantum measurement disturbance
- Guarantee information-theoretic security

**Key Metrics:**
- **QBER (Quantum Bit Error Rate)**: Percentage of errors in sifted bits
- **Threshold**: Typically ~11% (higher indicates eavesdropping)
- **Final Key**: Secure bits after privacy amplification

## 🔧 Local Development (Optional)

If you want to run locally with Streamlit:

1. Install dependencies:
   ```bash
   pip install streamlit qiskit qiskit-aer numpy pandas matplotlib
   ```

2. Run the app:
   ```bash
   streamlit run streamlit_app.py
   ```

3. Open browser at `http://localhost:8501`

## 📝 Files Included

- `index.html`: Main file for GitHub Pages deployment with stlite
- `streamlit_app.py`: Standalone Streamlit app (for local development)
- `README.md`: This documentation

## ⚠️ Important Notes

1. **First Load**: The app may take 10-30 seconds to load initially as it downloads Python packages (Qiskit, NumPy, etc.)
2. **Browser Compatibility**: Works best in Chrome, Firefox, Safari, and Edge (latest versions)
3. **Performance**: Large simulations (500+ bits) may take longer to compute in the browser
4. **Offline Capability**: After first load, the app can work offline (packages are cached)

## 🐛 Troubleshooting

### App doesn't load
- Check browser console for errors (F12)
- Try a different browser
- Clear browser cache and reload
- Wait a bit longer (initial load is slow)

### GitHub Pages not working
- Ensure repository is public
- Check that index.html is in root directory
- Verify GitHub Pages is enabled in Settings
- Wait 5-10 minutes after enabling Pages

### Simulation errors
- Try reducing number of bits
- Check that parameters are within valid ranges
- Refresh the page and try again

## 📚 Learn More

- [BB84 Protocol (Wikipedia)](https://en.wikipedia.org/wiki/BB84)
- [Qiskit Documentation](https://qiskit.org/documentation/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [stlite Repository](https://github.com/whitphx/stlite)

## 📄 License

This project is open source and available for educational purposes.

## 🤝 Contributing

Feel free to fork, modify, and enhance this simulator! If you find bugs or have suggestions, please open an issue.

## 👏 Acknowledgments

- **Charles Bennett & Gilles Brassard** for inventing the BB84 protocol
- **Qiskit team** for the quantum computing framework
- **Streamlit & stlite teams** for making web deployment easy
- **Pyodide project** for Python in WebAssembly

---

**Made with ❤️ for quantum cryptography education**
