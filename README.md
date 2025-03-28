# SNPedia Project

Welcome to our SNPedia Project! This project leverages the immense data from **SNPedia**, a comprehensive wiki-based bioinformatics database of over 100,000 single nucleotide polymorphisms (SNPs). Our goal is to provide an educational resource, enabling easy exploration and analysis of genetic data.

## Overview

The project encompasses several key components:
- **Data Extraction and Organization**: Using SNPedia as the source, we compile and structure a dataset in a relational database format for computational processing.
- **Web Application**: A user-friendly interface developed with Express.js enables users to upload genetic data, generate reports on significant SNPs, and explore the database in detail.

## Features

1. **Upload and Analyze**: Users can upload raw genetic data files (e.g., from 23andMe) to generate comprehensive reports highlighting important SNPs and their potential interpretations.
2. **Exploration Interface**: The web application provides an interface to browse all SNPs, view details, and access related scientific literature retrieved from SNPedia.

## Data Quality and Use

- The SNPedia data, while extensive, is community-driven and not guaranteed for medical use. It's suitable primarily for educational and informational purposes.
- The dataset follows a structured, normalized format (4NF) to improve data retrieval and management efficiency.

## Technical Implementation

- **Database**: MySQL database stores the SNP information. Only `SELECT` privileges are granted to the `snpedia_user` for security, following the principle of least privilege.
- **Security**: We employ prepared statements to mitigate SQL injection risks.
- **Technologies Used**: Node.js, Express.js, EJS for templating, MySQL.

## How to Run

1. **Setup the Database**:
    ```
    bash mysql -u root CREATE DATABASE snpedia_db; mysql -u root snpedia_db < snpedia_db.sql CREATE USER 'snpedia_user' IDENTIFIED BY 'password'; GRANT SELECT ON snpedia_db.* TO 'snpedia_user';
    ```

2. **Run the Application**:
    ```
    bash cd app/ npm install npm run dev
    ```


## Contribution and License

The project is licensed under the [Creative Commons Attribution-Noncommercial-Share Alike 3.0 US License](http://creativecommons.org/licenses/by-nc-sa/3.0/us/). Feel free to contribute by submitting issues or pull requests. We welcome collaboration and improvements!

## Acknowledgments

- Thanks to SNPedia for providing an invaluable repository of SNP data.
- Special mention to the open-source community for the tools and documentation used here.

For more details, visit [SNPedia](https://snpedia.com/).

This README aims to provide a clear overview of the project, its purpose, and how to get started, making your project accessible and informative to new contributors or users.