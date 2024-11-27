# NanoTrim
Efficient Barcode Demultiplexing and Sequence Trimming for Nanopore Sequencing Data.

---

## Introduction  
**NanoTrim** is a lightweight and user-friendly tool designed to preprocess Nanopore sequencing data. It efficiently handles:  
1. **Barcode demultiplexing**: Separate reads based on their associated barcodes.  
2. **Sequence trimming**: Remove unwanted sequences, such as primers or adapters, with high precision.  
3. **Customizable workflows**: Trim user-specified sequences at any region of the reads.  

With a focus on speed, accuracy, and usability, **NanoTrim** is an ideal choice for researchers working with Nanopore sequencing datasets.  

---

## Features  
- **Barcode Demultiplexing**: Automatically identifies and separates reads into barcode-specific groups.  
- **Flexible Sequence Trimming**: Supports both 5' and 3' end trimming for user-defined sequences.  
- **High Performance**: Optimized for large-scale datasets.  
- **Compatibility**: Accepts standard FASTQ/FASTA file formats.  

---

## Installation  
Clone the repository and install the required dependencies:  
```bash  
git clone https://github.com/your-username/NanoTrim.git  
cd NanoTrim  
pip install -r requirements.txt  
```  

---

## Usage  
Run **NanoTrim** from the command line:  
```bash  
python nanotrim.py --input input.fastq --barcode barcodes.txt --trim-seq AGCTTAGC --output output_directory
or
NanoTrim -h  
```  

### Command-Line Arguments  
- `--input`: Path to the input FASTQ/FASTA file.  
- `--barcode`: File containing barcode sequences for demultiplexing.  
- `--trim-seq`: Sequence to trim (e.g., adapter or primer).  
- `--output`: Directory for the output files.  

---

## Example  
### Input:  
- FASTQ file: `example.fastq`  
- Barcode file:  
```txt  
barcode1: AGCTTAGC  
barcode2: TCGATCGA  
```  

### Command:  
```bash  
python nanotrim.py --input example.fastq --barcode barcodes.txt --trim-seq AGCTTAGC --output results  
```  

### Output:  
- `results/barcode1.fastq`  
- `results/barcode2.fastq`  
- `results/unassigned.fastq`  

---

## License  
This project is licensed under the [MIT License](LICENSE).  

---

## Contributing  
We welcome contributions! Please feel free to submit issues or pull requests on [GitHub](https://github.com/linkoukou/NanoTrim).  

---

## Acknowledgements  
This software was inspired by the challenges of preprocessing Nanopore sequencing data and aims to simplify this step for the bioinformatics community.  

--- 

Feel free to modify this based on your preferences and software specifics!
