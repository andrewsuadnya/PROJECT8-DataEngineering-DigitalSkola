# Generating random words
https://wonderwords.readthedocs.io/en/latest/quickstart.html#the-randomsentence-class

# How to
1. Run `python3 -m venv env` to create virtual environment
2. Run `pip3 install -r requirements.txt` to install Python packages
3. Run `docker-compose up` to spin up Kafka broker
4. Run `python3 sentences_producer.py` to run the producer to produce data
5. Run `python3 analytics.py` to get the data stream from Kafka and run the sentiment analysis
