PubMed Paper Fetcher

Overview

This project is a command-line tool to fetch research papers from PubMed based on a user-specified query. The program identifies papers with at least one author affiliated with a pharmaceutical or biotech company and exports the results as a CSV file.

Features

Fetches papers using the PubMed API

Supports PubMed's full query syntax

Filters authors affiliated with non-academic institutions

Extracts the corresponding author's email

Saves results as a CSV file

Provides a command-line interface

Installation

Prerequisites

Python 3.8+

Poetry (Dependency Management)

Steps

Clone the repository:

git clone https://github.com/yourusername/pubmed-paper-fetcher.git
cd pubmed-paper-fetcher

Install dependencies using Poetry:

poetry install

Usage

Command-line Options

usage: get-papers-list [-h] [-d] [-f FILE] query

Fetch research papers from PubMed based on a query.

positional arguments:
  query                Search query for PubMed.

optional arguments:
  -h, --help          Show this help message and exit.
  -d, --debug         Enable debug logging.
  -f FILE, --file FILE  Output CSV file name.

Example Usage

Fetch papers and display output:

poetry run get-papers-list "cancer treatment"

Fetch papers and save to a file:

poetry run get-papers-list "cancer treatment" -f results.csv

Configuration

Setting Up PubMed API Access

Ensure you set your email for Entrez API access in pubmed_fetcher.py:

Entrez.email = "your-email@example.com"

Development

Running Locally

To test the script locally, run:

poetry run python pubmed_fetcher.py "cancer research"

Publishing to Test PyPI (Bonus)

Build the package:

poetry build

Publish to Test PyPI:

poetry publish --repository testpypi

License

This project is licensed under the MIT License.
