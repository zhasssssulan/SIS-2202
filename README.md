\documentclass[12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage{graphicx}
\usepackage{subcaption}
\usepackage{amsmath}
\usepackage{booktabs}
\usepackage{geometry}
\usepackage{hyperref}
\geometry{a4paper, margin=1in}

\title{Automated Essay Scoring Using Machine Learning}
\author{Student 1, Student 2, Student 3}
\date{Machine Learning Course \\ Professor Dr. Abdul Razaque \\ Semester Project}

\begin{document}

\maketitle

\begin{abstract}
This report presents the development of an Automated Essay Scoring (AES) system using machine learning techniques. The system analyzes student essays and predicts scores based on various linguistic and structural features. We implemented and compared multiple models including linear regression, random forest, and neural networks. Our best model achieved a Quadratic Weighted Kappa of 0.78 and R² score of 0.72, demonstrating the feasibility of automated essay assessment. The report details our methodology, results, and insights gained from the project.
\end{abstract}

\tableofcontents

\section{Introduction}
\subsection{Problem Statement}
Manual essay grading is time-consuming, subjective, and difficult to scale. Automated Essay Scoring (AES) systems address these challenges by providing consistent, immediate feedback.

\subsection{Objectives}
\begin{itemize}
\item Develop an AES system using machine learning
\item Compare different ML approaches for essay scoring
\item Identify key features that predict essay quality
\item Achieve performance comparable to human graders
\end{itemize}

\subsection{Significance}
AES systems can revolutionize educational assessment by providing scalable, consistent, and immediate feedback, particularly valuable in large-scale testing and online education platforms.

\section{Literature Review}
Brief overview of existing AES approaches including:
\begin{itemize}
\item E-rater by Educational Testing Service
\item Project Essay Grade (PEG)
\item Bayesian Essay Test Scoring System (BETSY)
\item Recent deep learning approaches
\end{itemize}

\section{Methodology}
\subsection{Dataset}
We used the Hewlett Foundation AES dataset containing approximately 13,000 essays across 8 different prompts, each scored by two human raters on a 1-6 scale.

\subsection{Data Preprocessing}
\subsubsection{Text Cleaning}
\begin{itemize}
\item Lowercasing and contraction fixing
\item Special character removal
\item Tokenization and sentence segmentation
\end{itemize}

\subsubsection{Feature Engineering}
We extracted four categories of features:
\begin{enumerate}
\item \textbf{Surface Features}: Word count, sentence count, paragraph count
\item \textbf{Lexical Features}: Vocabulary diversity, word sophistication
\item \textbf{Syntactic Features}: POS tag ratios, grammar complexity
\item \textbf{Readability Metrics}: Flesch-Kincaid, SMOG index
\end{enumerate}

\subsection{Models Implemented}
\begin{itemize}
\item \textbf{Baseline}: Linear Regression with basic features
\item \textbf{Random Forest}: Ensemble method with feature importance analysis
\item \textbf{Neural Network}: Multi-layer perceptron for complex pattern recognition
\end{itemize}

\subsection{Evaluation Metrics}
\begin{itemize}
\item Quadratic Weighted Kappa (QWK)
\item Mean Absolute Error (MAE)
\item Root Mean Square Error (RMSE)
\item R² Score
\item Accuracy within ±1 score point
\end{itemize}

\section{Experimental Results}
\subsection{Exploratory Data Analysis}
\begin{figure}[h]
\centering
\includegraphics[width=0.8\textwidth]{images/score_distribution.png}
\caption{Distribution of essay scores across different prompts}
\label{fig:score_dist}
\end{figure}

\subsection{Feature Analysis}
\begin{table}[h]
\centering
\begin{tabular}{@{}lc@{}}
\toprule
\textbf{Feature} & \textbf{Correlation with Score} \\ \midrule
Word Count & 0.45 \\
Lexical Diversity & 0.62 \\
Sentence Complexity & 0.51 \\
Transition Word Usage & 0.38 \\
\bottomrule
\end{tabular}
\caption{Correlation of features with essay scores}
\label{tab:correlations}
\end{table}

\subsection{Model Performance}
\begin{table}[h]
\centering
\begin{tabular}{@{}lcccc@{}}
\toprule
\textbf{Model} & \textbf{QWK} & \textbf{MAE} & \textbf{RMSE} & \textbf{R²} \\ \midrule
Baseline (Ridge) & 0.65 & 0.72 & 0.89 & 0.58 \\
Random Forest & 0.78 & 0.51 & 0.68 & 0.72 \\
Neural Network & 0.75 & 0.55 & 0.71 & 0.69 \\
\bottomrule
\end{tabular}
\caption{Performance comparison of different models}
\label{tab:performance}
\end{table}

\subsection{Error Analysis}
\begin{itemize}
\item Most errors occur in mid-range scores (3-4)
\item Extreme scores (1 and 6) are predicted more accurately
\item Longer essays show more consistent predictions
\end{itemize}

\section{Discussion}
\subsection{Key Findings}
\begin{itemize}
\item Random Forest performed best overall, balancing accuracy and interpretability
\item Lexical diversity and syntactic complexity were the most predictive features
\item Different essay prompts require different scoring models
\end{itemize}

\subsection{Limitations}
\begin{itemize}
\item Limited semantic understanding of essay content
\item Potential bias in training data
\item Difficulty scoring creative or unconventional essays
\end{itemize}

\subsection{Ethical Considerations}
We addressed potential biases by:
\begin{itemize}
\item Analyzing model fairness across different essay types
\item Providing transparency in scoring criteria
\item Recommending human review for borderline cases
\end{itemize}

\section{Conclusion and Future Work}
\subsection{Conclusion}
We successfully developed an AES system that achieves performance approaching human inter-rater reliability. The system demonstrates the feasibility of automated essay assessment for educational applications.

\subsection{Future Improvements}
\begin{enumerate}
\item Implement transformer-based models (BERT, GPT) for better semantic understanding
\item Develop multi-task learning to predict different scoring dimensions
