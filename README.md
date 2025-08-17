<div id="top"></div>

<div align="center">
  <br/>
  <h1>CLAIMGUARD</h1>
  <h3><em>Smart claims. Faster decisions. Lower risk.</em></h3>
  <p>An AI-powered application that automates the assessment of insurance claim risk, leveraging a RAG pipeline with Google's Gemini Pro for accurate and efficient analysis.</p>
  <br/>

  <img src="https://img.shields.io/badge/python-3.9+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/github/license/Aaditya231250/ClaimGuard?style=flat&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
  <img src="https://img.shields.io/github/last-commit/Aaditya231250/ClaimGuard?style=flat&logo=git&logoColor=white&color=0080ff" alt="last-commit">
  <img src="https://img.shields.io/github/languages/top/Aaditya231250/ClaimGuard?style=flat&color=0080ff" alt="repo-top-language">
  <img src="https://img.shields.io/github/languages/count/Aaditya231250/ClaimGuard?style=flat&color=0080ff" alt="repo-language-count">
</div>
<br>

---

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
    - [Project Index](#project-index)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Usage](#usage)
    - [Testing](#testing)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## Overview

ClaimGuard is an AI-powered application that automates the assessment of insurance claim risk, leveraging large language models for accurate and efficient analysis.

**Why ClaimGuard?**

This project streamlines insurance claim processing by automating risk assessment and providing a user-friendly interface. The core features include:

- **🔶 Automated Claim Risk Assessment:**  Quickly assesses claim validity and risk, reducing manual review time and human error.
- **🔷 Large Language Model Integration:** Leverages advanced AI for sophisticated analysis of complex documents, going beyond simple keyword matching.
- **🔶 Modular Design:**  Cleanly separated components (UI, processing, retrieval) facilitate easier maintenance, testing, and extension.
- **🔷 Reproducible Environment:**  `requirements.txt` ensures consistent setup across different machines, simplifying deployment and collaboration.
- **🔶 User-Friendly UI:**  Provides an intuitive Gradio interface for easy interaction and result visualization.
- **🔷 Ensemble Retriever:** Combines BM25 and vectorstore retrieval for highly accurate and efficient context retrieval.

---

## Features

- **🤖 AI-Powered Risk Scoring:** Leverages the Gemini 1.5 Pro model to intelligently analyze documents and generate a comprehensive risk assessment, including a validity score and violation summaries.
- **🔍 Hybrid Search RAG Pipeline:** Implements an advanced ensemble retriever combining keyword-based (BM25) and semantic vector-based (ChromaDB) search for highly accurate context retrieval from policy and claim documents.
- **📄 PDF Document Processing:** Ingests and intelligently parses complex PDF documents (`.pdf`), extracting text and structuring it for analysis.
- **🌐 Interactive Web UI:** A user-friendly interface built with Gradio allows for easy uploading of claim/policy documents and clear visualisation of the results.
- **📦 Modular & Scalable Architecture:** Decoupled components for document processing, retrieval, prediction, and UI ensure the system is easy to maintain, test, and scale.
- **⚙️ Reproducible Environment:** A detailed `requirements.txt` file ensures a consistent and hassle-free setup for all users and developers.

---

## 🛠️ Technology Stack

- **LLM & Frameworks:** LangChain, Google Gemini Pro
- **Vector Database:** ChromaDB
- **Retrieval:** Ensemble Retriever (BM25 & Vector Search)
- **UI:** Gradio
- **Document Parsing:** PyMuPDF

---

## Project Structure

```sh
└── ClaimGuard/
    ├── Final Reports
    │   ├── Claim Report 1.pdf
    │   ├── Claim Report 2.pdf
    │   ├── Claim Report 3.pdf
    │   ├── Claim Report 4.pdf
    │   ├── Claim Report 5.pdf
    │   └── Error Report.pdf
    ├── README.md
    ├── data
    │   ├── car.pdf
    │   ├── goog-10-k-2023.pdf
    │   └── health.pdf
    ├── requirements.txt
    └── src
        ├── .DS_Store
        ├── __init__.py
        ├── claim_risk_predictor.py
        ├── document_processor.py
        ├── main.py
        ├── retriever.py
        ├── ui.py
        └── utils
```

### Project Index

<details open>
	<summary><b><code>CLAIMGUARD/</code></b></summary>
	<!-- __root__ Submodule -->
	<details>
		<summary><b>__root__</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ __root__</b></code>
			<table style='width: 100%; border-collapse: collapse;'>
			<thead>
				<tr style='background-color: #f8f9fa;'>
					<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
					<th style='text-align: left; padding: 8px;'>Summary</th>
				</tr>
			</thead>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/requirements.txt'>requirements.txt</a></b></td>
					<td style='padding: 8px;'>- The requirements file specifies the projects dependencies<br>- It lists all necessary Python packages and their versions, enabling reproducible environment creation for development and deployment<br>- These packages support various functionalities, including web frameworks (FastAPI, Starlette), language models (Langchain, Google Generative AI), and database interactions (ChromaDB)<br>- The file facilitates consistent setup across different machines.</td>
				</tr>
			</table>
		</blockquote>
	</details>
	<!-- src Submodule -->
	<details>
		<summary><b>src</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ src</b></code>
			<table style='width: 100%; border-collapse: collapse;'>
			<thead>
				<tr style='background-color: #f8f9fa;'>
					<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
					<th style='text-align: left; padding: 8px;'>Summary</th>
				</tr>
			</thead>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/src/claim_risk_predictor.py'>claim_risk_predictor.py</a></b></td>
					<td style='padding: 8px;'>- ClaimRiskPredictor assesses claim validity and risk<br>- It leverages a large language model to analyze claim reports against policy terms and conditions, generating a risk score, identifying violations and gaps, and recommending actions<br>- The system incorporates document processing, retrieval, and a custom prompt for structured JSON output<br>- Metadata on processed documents and relevant sections is also provided.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/src/ui.py'>ui.py</a></b></td>
					<td style='padding: 8px;'>- The <code>src/ui.py</code> file constructs a Gradio-based user interface for an insurance claim risk analysis application<br>- It allows users to upload claim and policy documents, specify an analysis query, and receive a risk assessment report<br>- The UI handles file uploads, processing via a <code>ClaimRiskPredictor</code>, and presents results in a user-friendly format, integrating seamlessly with the backend prediction logic.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/src/document_processor.py'>document_processor.py</a></b></td>
					<td style='padding: 8px;'>- DocumentProcessor handles the ingestion and processing of terms and conditions and claim report documents<br>- It extracts text, splits it into manageable chunks, identifies document structure, and categorizes content by section<br>- The processed data, including metadata and section titles, is packaged into a structured format for downstream tasks within the larger application.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/src/retriever.py'>retriever.py</a></b></td>
					<td style='padding: 8px;'>- The <code>retriever.py</code> module implements a retrieval system for the project<br>- It prepares documents, using both BM25 and vectorstore-based retrievers, to create an ensemble retriever<br>- This system efficiently retrieves relevant context from a combined document set based on a given query, logging retrieval statistics for monitoring and debugging<br>- The output consists of a ranked list of relevant documents.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/src/main.py'>main.py</a></b></td>
					<td style='padding: 8px;'>- The <code>main.py</code> script orchestrates claim risk assessment<br>- It utilizes the <code>ClaimRiskPredictor</code> class to analyze claim and policy documents, processing a user query to generate a structured risk assessment result, which is then outputted as JSON<br>- This script serves as the primary entry point for the application, integrating data input and output within the larger claim risk prediction system.</td>
				</tr>
			</table>
			<!-- utils Submodule -->
			<details>
				<summary><b>utils</b></summary>
				<blockquote>
					<div class='directory-path' style='padding: 8px 0; color: #666;'>
						<code><b>⦿ src.utils</b></code>
					<table style='width: 100%; border-collapse: collapse;'>
					<thead>
						<tr style='background-color: #f8f9fa;'>
							<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
							<th style='text-align: left; padding: 8px;'>Summary</th>
						</tr>
					</thead>
						<tr style='border-bottom: 1px solid #eee;'>
							<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/src/utils/logging.py'>logging.py</a></b></td>
							<td style='padding: 8px;'>- Logging functionality is established for the application<br>- The <code>logging.py</code> module centralizes logging configuration, providing a consistent method for recording application events<br>- This ensures consistent logging across the entire project, simplifying debugging and monitoring<br>- The setup function returns a logger instance, readily accessible throughout the applications modules.</td>
						</tr>
						<tr style='border-bottom: 1px solid #eee;'>
							<td style='padding: 8px;'><b><a href='https://github.com/Aaditya231250/ClaimGuard/blob/master/src/utils/text_preprocessing.py'>text_preprocessing.py</a></b></td>
							<td style='padding: 8px;'>- Text_preprocessing.py` provides text cleaning and document type detection functionalities<br>- Cleaning normalizes text by removing unnecessary characters and extra whitespace<br>- Document type detection analyzes text content, identifying it as a claim report, policy document, medical report, invoice, correspondence, or other, based on keyword presence<br>- These utilities support the core document processing pipeline within the larger application.</td>
						</tr>
					</table>
				</blockquote>
			</details>
		</blockquote>
	</details>
</details>

---

## Getting Started

### Prerequisites

This project requires the following dependencies:

- **Programming Language:** Python
- **Package Manager:** Pip

### Installation

Build ClaimGuard from the source and install dependencies:

1. **Clone the repository:**

    ```sh
    ❯ git clone https://github.com/Aaditya231250/ClaimGuard
    ```

2. **Navigate to the project directory:**

    ```sh
    ❯ cd ClaimGuard
    ```

### Usage

Run the project with:

**Using [pip](https://pypi.org/project/pip/):**
```sh
python main.py
```

---

## Contributing

- **💬 [Join the Discussions](https://github.com/Aaditya231250/ClaimGuard/discussions)**: Share your insights, provide feedback, or ask questions.
- **🐛 [Report Issues](https://github.com/Aaditya231250/ClaimGuard/issues)**: Submit bugs found or log feature requests for the `ClaimGuard` project.
- **💡 [Submit Pull Requests](https://github.com/Aaditya231250/ClaimGuard/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your github account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/Aaditya231250/ClaimGuard
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to github**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="left">
   <a href="https://github.com{/Aaditya231250/ClaimGuard/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=Aaditya231250/ClaimGuard">
   </a>
</p>
</details>

---

## License

Claimguard is protected under the [LICENSE](https://choosealicense.com/licenses) License. For more details, refer to the [LICENSE](https://choosealicense.com/licenses/) file.

---

## Acknowledgments

- Credit `contributors`, `inspiration`, `references`, etc.

<div align="right">

[![][back-to-top]](#top)

</div>


[back-to-top]: https://img.shields.io/badge/-BACK_TO_TOP-151515?style=flat-square


---
