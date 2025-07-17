🌐 **View this project as a live tutorial site:**  
👉 [https://sophosapien.github.io/GithubTutorial/](https://sophosapien.github.io/GithubTutorial/)
---

# 📄Github Tutorial using Mini Bioinformatics Project

## 🔬 FASTQ Quality Check  

This is a beginner-friendly, reproducible bioinformatics mini project to learn version control:

### 🔧 Skills/Concepts You’ll Practice
- Creating folders and files in WSL
- Using bash commands like mkdir, cd, git init, fastqc
- Tracking changes in Git and committing them
- Running FastQC on a real FASTQ file
- Using GitHub Desktop to push your repo online
- Viewing an HTML QC report from FastQC


### 🧰 Software & Tools

|| Tool/Software        | Purpose                                              |
|-|----------------------|------------------------------------------------------|
|✅| **Git**              | Version control to track your project                |
|✅| **GitHub Desktop**   | GUI to push your local project to GitHub             |
|✅| **GitHub account**   | To host your project repo                            |
|✅| **Visual Studio Code** | To edit and manage files (README, scripts, etc.)   |
|✅| **WSL with Ubuntu**  | Run Linux-based bioinformatics tools on Windows      |
|✅| **FastQC**           | Tool to perform quality control of FASTQ files       |
|✅| **Web browser**      | To download data and view results     |



### 📁 Project Structure

```bash
fastq-qc-practice/
├── README.md                      # Project instructions and overview
├── data/                          # Contains input FASTQ files
│   └── test.fastq                 # Real downloaded FASTQ file
├── results/                       # Output folder for FastQC reports
│   └── test_fastqc.html
├── scripts/                       # (Optional) Shell scripts or analysis tools
├── docs/                          # (Optional) Additional documentation
```
<br>

## 🧑‍🔬 Step-by-Step Instructions
### 1. Create your project folder
In WSL or Explorer:

```bash
mkdir -p /mnt/d/biprojects/fastq-qc-practice

```

### 2. Initialize Git locally

```bash
cd /mnt/d/biprojects/fastq-qc-practice
git init

```

### 3. Create a README file

Use VS Code to create a `README.md`, paste this file, and save it.

```
# Practice Project

This is a practice bioinformatics project to learn Git, GitHub, VS Code, and command-line tools.

## Goal
- Download an example FASTQ file
- Run FastQC for quality check
- Version control the entire workflow
```

### 4. Add folders

```bash
mkdir data results scripts docs
touch data/.gitkeep results/.gitkeep scripts/.gitkeep docs/.gitkeep

```

### 5. Commit changes to Git

```bash
git add .
git commit -m "Add project structure and README"

```

### 6. Install FastQC in WSL Ubuntu (if not present)

```bash
sudo apt update
sudo apt install fastqc

```

### 7. Create your own test FASTQ file OR use the file in `data/test.fastq`

```bash
cat > data/test.fastq <<EOF
@SEQ_ID
GATTTGGGGTTTAAAGGGTGCCCGATAG
+
IIIIIIIIIIIIIIIIIIIIIIIIIIII
@SEQ_ID2
TGGGTTTAAAGGGTGCCCGATAGGCTA
+
IIIIIIIIIIIIIIIIIIIIIIIIIIII
EOF

```

### 8. Run FastQC

```bash
fastqc data/test.fastq -o results
```

### 9. Commit results

```bash
git add results/
git commit -m "Add FastQC report for test.fastq"

```

### 10. Push to GitHub using GitHub Desktop

- Open GitHub Desktop
- Add local repo
- Click **“Publish Repository”**
- Fill in repo name + description
- Uncheck private
- Do not initialize with README
- Click **Publish**

---
 > 🎉Now your project is live!<br>

<br>

### 🟩License

This project is MIT Licensed – feel free to fork, adapt, and share!

[@sophosapien](https://github.com/sophosapien)

