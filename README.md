%-------------------------------------
% LaTeX Resume for Software Engineers
% Author : Leslie Cheng
% License : MIT
%-------------------------------------

\documentclass[letterpaper,12pt]{article}[leftmargin=*]

\usepackage[empty]{fullpage}
\usepackage{enumitem}
\usepackage[pdftex]{hyperref}
\usepackage{fontawesome}
\usepackage[sfdefault,light]{FiraSans}
\usepackage[T1]{fontenc}
\usepackage{anyfontsize}
\usepackage{xcolor}

%-------------------------------------------------- SETTINGS HERE --------------------------------------------------
% Header settings
\def \fullname {Shailendra Jain}
\def \subtitle {}

\def \linkedinicon {\faLinkedin}
\def \linkedinlink {https://www.linkedin.com/in/shailendrajain28/}
\def \linkedintext {/shailendrajain28}

\def \phoneicon {\faPhone}
\def \phonetext {+91-9967219623}

\def \emailicon {\faEnvelope}
\def \emaillink {mailto:shailendrajain28@gmail.com}
\def \emailtext {shailendrajain28@gmail.com}

\def \githubicon {\faGithub}
\def \githublink {https://github.com/shailendrajain2892}
\def \githubtext {/shailendrajain2892}

\def \websiteicon {\faGlobe}
\def \websitelink {https://medium.com/@shailendrajain28}
\def \websitetext {/shailendrajain28}

\def \headertype {\doublecol} % \singlecol or \doublecol

% Misc settings
\def \entryspacing {-0pt}

\def \bulletstyle {\faAngleRight}

% Define colours
\definecolor{primary}{HTML}{000000}
\definecolor{secondary}{HTML}{0D47A1}
\definecolor{accent}{HTML}{263238}
\definecolor{links}{HTML}{1565C0}

%------------------------------------------------------------------------------------------------------------------- 

% Defines to make listing easier
\def \linkedin {\linkedinicon \hspace{3pt}\href{\linkedinlink}{\linkedintext}}
\def \phone {\phoneicon \hspace{3pt}{ \phonetext}}
\def \email {\emailicon \hspace{3pt}\href{\emaillink}{\emailtext}}
\def \github {\githubicon \hspace{3pt}\href{\githublink}{\githubtext}}
\def \website {\websiteicon \hspace{3pt}\href{\websitelink}{\websitetext}}

% Adjust margins
\addtolength{\oddsidemargin}{-0.55in}
\addtolength{\evensidemargin}{-0.55in}
\addtolength{\textwidth}{1.1in}
\addtolength{\topmargin}{-0.6in}
\addtolength{\textheight}{1.1in}

% Define the link colours
\hypersetup{
    colorlinks=true,
    urlcolor=links,
}

% Set the margin alignment 
\raggedbottom
\raggedright
\setlength{\tabcolsep}{0in}

%-------------------------
% Custom commands

% Sections
\renewcommand{\section}[2]{\vspace{5pt}
  \colorbox{secondary}{\color{white}\raggedbottom\normalsize\textbf{{#1}{\hspace{7pt}#2}}}
}

% Entry start and end, for spacing
\newcommand{\resumeEntryStart}{\begin{itemize}[leftmargin=2.5mm]}
\newcommand{\resumeEntryEnd}{\end{itemize}\vspace{\entryspacing}}

% Itemized list for the bullet points under an entry, if necessary
\newcommand{\resumeItemListStart}{\begin{itemize}[leftmargin=4.5mm]}
\newcommand{\resumeItemListEnd}{\end{itemize}}

% Resume item
\renewcommand{\labelitemii}{\bulletstyle}
\newcommand{\resumeItem}[1]{
  \item\small{
    {#1 \vspace{-2pt}}
  }
}

% Entry with title, subheading, date(s), and location
\newcommand{\resumeEntryTSDL}[4]{
  \vspace{-1pt}\item[]
    \begin{tabular*}{0.97\textwidth}{l@{\extracolsep{\fill}}r}
      \textbf{\color{primary}#1} & {\firabook\color{accent}\small#2} \\
      \textit{\color{accent}\small#3} & \textit{\color{accent}\small#4} \\
    \end{tabular*}\vspace{-6pt}
}

% Entry with title and date(s)
\newcommand{\resumeEntryTD}[2]{
  \vspace{-1pt}\item[]
    \begin{tabular*}{0.97\textwidth}{l@{\extracolsep{\fill}}r}
      \textbf{\color{primary}#1} & {\firabook\color{accent}\small#2} \\
    \end{tabular*}\vspace{-6pt}
}

% Entry for special (skills)
\newcommand{\resumeEntryS}[2]{
  \item[]\small{
    \textbf{\color{primary}#1 }{ #2 \vspace{-6pt}}
  }
}

% Double column header
\newcommand{\doublecol}[6]{
  \begin{tabular*}{\textwidth}{l@{\extracolsep{\fill}}r}
    {
      \begin{tabular}[c]{l}
        \fontsize{35}{45}\selectfont{\color{primary}{{\textbf{\fullname}}}} \\
        {\textit{\subtitle}} % You could add a subtitle here
      \end{tabular}
    } & {
      \begin{tabular}[c]{l@{\hspace{1.5em}}l}
        {\small#4} & {\small#1} \\
        {\small#5} & {\small#2} \\
        {\small#6} & {\small#3}
      \end{tabular}
    }
  \end{tabular*}
}

% Single column header
\newcommand{\singlecol}[6]{
  \begin{tabular*}{\textwidth}{l@{\extracolsep{\fill}}r}
    {
      \begin{tabular}[b]{l}
        \fontsize{35}{45}\selectfont{\color{primary}{{\textbf{\fullname}}}} \\
        {\textit{\subtitle}} % You could add a subtitle here
      \end{tabular}
    } & {
      \begin{tabular}[c]{l}
        {\small#1} \\
        {\small#2} \\
        {\small#3} \\
        {\small#4} \\
        {\small#5} \\
        {\small#6}
      \end{tabular}
    }
  \end{tabular*}
}

\begin{document}
%-------------------------------------------------- BEGIN HERE --------------------------------------------------

%---------------------------------------------------- HEADER ----------------------------------------------------

\headertype{\linkedin}{\github}{\website}{\phone}{\email}{} % Set the order of items here
\vspace{-10pt} % Set a negative value to push the body up, and the opposite

%-------------------------------------------------- EDUCATION --------------------------------------------------
\section{\faGraduationCap}{Education}

  \resumeEntryStart
    \resumeEntryTSDL
      {Jabalpur Engineering College}{2009 -- 2013}
      {Bachelor of Engineering, Information Technology}{Jabalpur, Madhya Pradesh}
  \resumeEntryEnd
%-------------------------------------------------- PROGRAMMING SKILLS --------------------------------------------------
\section{\faGears}{Skills}
 \resumeEntryStart
  \resumeEntryS{Programming Languages } {Python, Machine Learning, C, C++, }
  \resumeEntryS{Libraries \& Tools } {Sklearn, Numpy, Pandas, Matplotlib, Seaborn, Shell Scripting, IPC}
  \resumeEntryS{Algorthims used } {Linear Regression, Logistic Regression, Decision Tree, Voting Classifiers}
 \resumeEntryEnd
%-------------------------------------------------- EXPERIENCE --------------------------------------------------
\section{\faPieChart}{Experience \& Projects}

  \resumeEntryStart
    \resumeEntryTSDL
      {Machine Learning Masters Program from Grey Atom School of Data Science}{Jan. 2019 -- June 2019}
      {Student}{Mumbai, Maharashtra}
    \resumeItemListStart
      \resumeItem {As a Data Science Immersive student at Grey Atom, I've studied the methodological and mathematical foundations of data science and machine learning, as well as practical, hands-on skills. Classwork ranged from in-class projects and Kaggle competitions, to personal projects focused on real-world applications of data science principles and best practices.}
      \resumeItem {\textbf{Predicting H1B the case Status using Classification} \textbf{-} Predicted the case status of an application submitted by the employer to hire non-immigrant workers under the H-1B visa program, using Decision Tree, Random Forest and Multi class model.}
      \resumeItem {\textbf{Detect Pink panther and Little man in a given Video using Deep Learning and Open CV} \textbf{-} Classified pink panther and little man images from a given video by extracting all the images and training the vgg16 model. }      
    \resumeItemListEnd
  \resumeEntryEnd
  
  \resumeEntryStart
    \resumeEntryTSDL
      {Bank Of America}{June 2017 -- Present}
      {Senior Software Engineer}{Mumbai, Maharashtra}
    \resumeItemListStart
      \resumeItem {Working on development project where we are trying to build One Trading Application for the all line of business, instead of multiple, which can save a lot of operational cost of managing multiple Trading Applications}
      \resumeItem {we are using Service Based framework, where processing is separated by different services}
      \resumeItem {For UI we are React based Framework. UI and Backbend are connected using Rester end points.}
      \resumeItem {we are using Service Based framework, where processing is separated by different services}
      \resumeItem {Developed a script in python which combines two different tables into one. These tables contains events and deal level information. This table is then later used for regulatory reporting purpose.}     
      \resumeItem {My roles in this team as a developer. Here we follow agile process, where we have 15 days sprint. In every sprint task is assigned to us and within that sprint we need to complete the given task with unit testing and deploy it to production. We use here Jira, Bit Bucket, and SVN to follow agile process.}
    \resumeItemListEnd
  \resumeEntryEnd

  \resumeEntryStart
    \resumeEntryTSDL
      {Accenture}{Feb. 2016 -- June 2017}
      {Software Engineer}{Mumbai, Maharashtra}
    \resumeItemListStart
      \resumeItem {Maintained a desktop application, which is used by MetLife client for displaying Illustration for their customer. MetLife representatives enter input data of customer via this application like customer name, age, sex, smoker status, risk class etc. to Illustrate insurance policy. This application on the basis provided input data and insurance policy, generate reports for its customer. Generated Report contains multiple columns like premium, net cash value, dividend and death benefit with year wise data. For example in first year how much premium you need to pay, how much net cash value you will have in your account, how much dividend you will get and how much death benefit you will have. Report displays these information for multiple years for year 1 to year 100 depends on type of policy. For ex whole life policy Illustrates information for 120 years and term policy illustrates information till the year policy has taken.}
      \resumeItem {I was a software developer in this project. I was responsible here for requirement understanding, providing estimation, software development, testing, and deployment and build management via version control system.}
    \resumeItemListEnd
  \resumeEntryEnd

  \resumeEntryStart
    \resumeEntryTSDL
      {Tata Consultance Services}{June 2013 -- Feb. 2017}
      {System Engineer}{Mumbai, Maharashtra}
    \resumeItemListStart
        \resumeItem {I have worked on Trading Platform system here.}
        \resumeItem {This project has 4 component, NET, DS(data subsystem), MKT(Matching engine), PT (post trade).In this trading platform there is front end which is a desktop based application through which End users take login and perform trading. NET component responsible with initial validation of data packet, routing and login of users.MKT component responsible for order Matching. PT component is responsible for serving inquiry. DS component is responsible for maintaining master data of all users.

I had worked in TCS for NSE client.
For NSE client requirement I have worked in all SDLC phases. I have worked on NET module, which is one of the components of trading system. For this module, I have worked from requirement analysis to design implementation, development, unit testing, system testing, performance testing. Now it’s running LIVE. This module was performance oriented. I have also worked on performance of this module and brought down it's latency by optimizing its code.
This whole module was on C, C++, STL, Socket programming, multithreading, and SMFS database on Linux machine. I have good command over Linux command and shell scripting. I have acquainted knowledge of capital market trading system. I have successfully passed NSE capital market beginners module exam.
}
        \resumeItem {Provided extraordinary and exceptional customer service to the masses}
    \resumeItemListEnd
  \resumeEntryEnd

\end{document}
