# DATASCI 350 - Quiz 04

## SQL Queries

In this quiz, you will test your SQL skills through queries using two tables. The tables refer to Nobel Prize winners and their respective personal information. The questions are available in the `quiz04.ipynb` file. The tables are as follows.

### Table Structures

#### nobel_laureates

This table contains personal and award information about Nobel Prize winners:

| Column        | Type          | Description                                    |
|---------------|---------------|------------------------------------------------|
| id            | INTEGER       | Primary key (auto-increments in SQLite)        |
| name          | TEXT          | Full name of the laureate                      |
| field         | TEXT          | Field of study (Physics, Chemistry, Physiology)|
| year_award    | INTEGER       | Year the Nobel Prize was awarded               |
| prize_amount  | REAL          | Prize amount in USD                            |
| age_at_award  | INTEGER       | Age of the laureate when receiving the award   |

#### discoveries

This table contains information about the laureates' groundbreaking discoveries:

| Column          | Type          | Description                                    |
|-----------------|---------------|------------------------------------------------|
| id              | INTEGER       | Primary key (auto-increments in SQLite)        |
| laureate_id     | INTEGER       | Foreign key referencing nobel_laureates(id)    |
| discovery       | TEXT          | Description of the scientific discovery        |
| year_discovery  | INTEGER       | Year when the discovery was made               |
| research_funding| REAL          | Amount of funding received for the research    |
| citation_count  | INTEGER       | Number of citations for the discovery          |

### Sample Data

#### nobel_laureates table data:

| id | name               | field      | year_award | prize_amount | age_at_award |
|----|--------------------|------------|------------|--------------|--------------|
| 1  | Marie Curie        | Physics    | 1903       | 15000.00     | 36           |
| 2  | Dorothy Hodgkin    | Chemistry  | 1964       | 273000.00    | 54           |
| 3  | Barbara McClintock | Physiology | 1983       | 1900000.00   | 81           |
| 4  | Richard Feynman    | Physics    | 1965       | 282000.00    | 47           |
| 5  | Frederick Sanger   | Chemistry  | 1958       | 250000.00    | 40           |
| 6  | Werner Heisenberg  | Physics    | 1932       | 159917.00    | 31           |
| 7  | Gertrude Elion     | Physiology | 1988       | 2100000.00   | 70           |
| 8  | Linus Pauling      | Chemistry  | 1954       | 236000.00    | 53           |
| 9  | Max Planck         | Physics    | 1918       | 38840.00     | 60           |
| 10 | Elizabeth Blackburn| Physiology | 2009       | 10000000.00  | 61           |

#### discoveries table data:

| id | laureate_id | discovery                            | year_discovery | research_funding | citation_count |
|----|-------------|--------------------------------------|----------------|------------------|----------------|
| 1  | 1           | Discovery of Radium and Polonium     | 1898           | 5000.00          | 12500          |
| 2  | 2           | Structure of Vitamin B12             | 1954           | 30000.00         | 8900           |
| 3  | 3           | Mobile Genetic Elements              | 1950           | 35000.00         | 7800           |
| 4  | 4           | Quantum Electrodynamics              | 1948           | 25000.00         | 13400          |
| 5  | 5           | Protein and Insulin Sequencing       | 1951           | 28000.00         | 9500           |
| 6  | 6           | Uncertainty Principle                | 1927           | 8000.00          | 9800           |
| 7  | 7           | Drug Development Through Rational Design | 1980       | 150000.00        | 9200           |
| 8  | 8           | Chemical Bond Nature                 | 1931           | 15000.00         | 11200          |
| 9  | 9           | Quantum Theory                       | 1900           | 3000.00          | 14000          |
| 10 | 10          | Telomeres and Telomerase             | 1984           | 180000.00        | 10500          |

### Relationships

- Each laureate in `nobel_laureates` has exactly one corresponding discovery in the `discoveries` table
- The tables are linked through the `laureate_id` foreign key in the `discoveries` table

### Deliverables

Please submit only your `.ipynb` file containing the queries on Canvas.

Good luck! 😉