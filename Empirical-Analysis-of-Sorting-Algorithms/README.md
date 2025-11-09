# Empirical Analysis of Sorting Algorithms

## Assignment Overview
This project implements and analyzes the time complexity of four sorting algorithms:
- **Bubble Sort** (O(n²))
- **Selection Sort** (O(n²))
- **Insertion Sort** (O(n²) worst, O(n) best)
- **Merge Sort** (O(n log n))

## Project Structure
```
algo/
├── sorting_analysis.ipynb      # Main Jupyter notebook with analysis
├── requirements.txt            # Python dependencies
├── README.md                   # This file
├── sorting_results.csv         # Generated: Detailed timing results
├── individual_algorithms.png   # Generated: Individual algorithm plots
├── sorting_comparison.png      # Generated: Comparison plot
└── bar_comparison.png          # Generated: Bar chart comparison
```

## Installation

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook

### Setup
1. Install required packages:
```bash
pip install -r requirements.txt
```

2. Launch Jupyter Notebook:
```bash
jupyter notebook
```

3. Open `sorting_analysis.ipynb` and run all cells

## Test Arrays
As per assignment requirements:
- **Arr1**: n=5   → [1, 2, 3, 4, 5]
- **Arr2**: n=10  → [1, 2, ..., 10]
- **Arr3**: n=50  → [1, 2, ..., 50]
- **Arr4**: n=100 → [1, 2, ..., 100]

## Methodology
1. **Implementation**: All four sorting algorithms implemented in Python
2. **Timing**: Using `time.perf_counter()` for high-precision measurements
3. **Multiple Runs**: Each test runs 5 times and results are averaged
4. **Visualization**: Multiple plots showing performance comparison
5. **Analysis**: Detailed empirical analysis comparing theoretical vs actual performance

## Expected Results

### Time Complexity Patterns
- **O(n²) algorithms** (Bubble, Selection, Insertion): Show quadratic growth
- **O(n log n) algorithm** (Merge Sort): Shows logarithmic-linear growth
- **Best Case Advantage**: Insertion Sort excels on already sorted data

### Key Findings
- For small arrays (n<50): Simple algorithms are competitive
- For large arrays (n≥100): Merge Sort dominates
- Insertion Sort performs best on sorted/nearly sorted data
- Merge Sort maintains consistent O(n log n) performance

## Outputs

### Generated Files
1. **sorting_results.csv**: Detailed timing data in tabular format
2. **individual_algorithms.png**: 2x2 subplot showing each algorithm's performance
3. **sorting_comparison.png**: Line plot comparing all algorithms
4. **bar_comparison.png**: Bar charts for each input size

### Console Output
- Algorithm implementations with test cases
- Detailed timing results for each algorithm and array size
- Comprehensive analysis report
- Statistical summary (average, min, max, std deviation)

## How to Run

### Quick Start
```bash
# Install dependencies
pip install numpy pandas matplotlib jupyter

# Launch Jupyter
jupyter notebook sorting_analysis.ipynb
```

### Running All Cells
In Jupyter Notebook:
1. Click **Kernel** → **Restart & Run All**
2. Wait for all cells to execute
3. View results, plots, and analysis

### Individual Sections
You can also run cells individually to:
- Test specific algorithms
- Modify input arrays
- Customize visualizations
- Export different data formats

## Customization

### Adding More Array Sizes
```python
arr5 = list(range(1, 201))  # n=200
test_arrays['Arr5 (n=200)'] = arr5
```

### Changing Number of Runs
```python
NUM_RUNS = 10  # Increase for more accurate averaging
```

### Testing Unsorted Arrays
```python
import random
arr_random = list(range(1, 101))
random.shuffle(arr_random)
```

## Assignment Requirements Checklist
- ✅ Implementation of 4 sorting algorithms
- ✅ Testing on 4 different array sizes (5, 10, 50, 100)
- ✅ High-precision timer (time.perf_counter())
- ✅ Multiple runs (5 runs per size)
- ✅ Average execution time calculation
- ✅ Plots with X-axis: Input Size, Y-axis: Time
- ✅ Detailed comparison and analysis
- ✅ Comprehensive report with observations

## Technical Details

### Timing Precision
- Uses `time.perf_counter()` for nanosecond precision
- Results reported in microseconds (μs) for readability
- Each array is copied before sorting to ensure fair comparison

### Algorithm Implementations
All algorithms include:
- Type hints for better code clarity
- Docstrings explaining complexity
- Array copying to avoid in-place modification
- Test cases for verification

## Author Notes
This implementation focuses on **empirical analysis** with actual measurements rather than just theoretical complexity. The sorted arrays test the best-case scenario, making Insertion Sort particularly efficient.

For real-world applications:
- Use built-in `sorted()` or `list.sort()` (Timsort - O(n log n))
- Consider Quick Sort for general-purpose sorting
- Use Insertion Sort for small or nearly sorted data

## References
- Time Complexity Analysis: Big O Notation
- Python's `time` module documentation
- Matplotlib visualization library
- Pandas for data analysis

---

**Assignment**: Empirical Analysis of Sorting Algorithms  
**Language**: Python  
**Tools**: Jupyter Notebook, NumPy, Pandas, Matplotlib
