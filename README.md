# Stream Analytics with Kafka and Python

## Overview
This project demonstrates real-time text stream processing using Kafka and Python. The project includes generating random sentences, sending them to Kafka, consuming these messages, and performing sentiment analysis.

## Project Structure
- `.gitignore`: Specifies files and directories to be ignored by Git.
- `Readme.md`: Documentation of the project.
- `analytics.py`: Consumes messages from Kafka and performs sentiment analysis.
- `docker-compose.yml`: Configuration for running Kafka, Zookeeper, and other services using Docker.
- `requirements.txt`: List of Python dependencies required for the project.
- `sentences_producer.py`: Produces random sentences and sends them to Kafka.
- `sentiment_analysis.py`: Contains functions or classes for sentiment analysis.

## Getting Started

### Prerequisites
- Docker and Docker Compose
- Python 3.x
- Kafka

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd stream-analytics-main
   ```

2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Start Docker services:
   ```bash
   docker-compose up
   ```

### Usage

1. Run the Kafka producer to generate and send random sentences:
   ```bash
   python sentences_producer.py
   ```

2. Run the Kafka consumer to consume messages and perform sentiment analysis:
   ```bash
   python analytics.py
   ```

### File Descriptions

- **sentences_producer.py**: Generates random sentences and sends them to a Kafka topic named `sentences`.
- **analytics.py**: Consumes messages from the `sentences` topic in Kafka and performs sentiment analysis using functions defined in `sentiment_analysis.py`.
- **sentiment_analysis.py**: Contains the logic for analyzing the sentiment of given sentences.

### Example Output

- **Producer Output**:
  ```
  Produced message on topic sentences with value of {"sentence": "The placid prayer changes carry."}
  ```

- **Consumer Output**:
  ```
  {'text': 'The placid prayer changes carry.', 'sentiment': 'negative'}
  ```
