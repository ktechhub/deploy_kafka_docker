# deploy_kafka_docker
Deploy Kafka on Docker. Play with it using Python.

## YouTube Video
[https://www.youtube.com/watch?v=CEZ1VJW1duo](https://www.youtube.com/watch?v=CEZ1VJW1duo)


## Start the docker-compose with console log output

```sh
docker-compose up
```

## Run it in detach mode
```sh
docker-compose up -d
```

## Stop Everything
```sh
docker-compose down
```

## Python
Create a virtualenv and install the requirements file

```sh
pip install -r requirements.txt
```

## Run consumer 
```sh
python consumer.py
```

## Run producer 
```sh
python producer.py
```

### Producer Sample Output
```sh
{'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:15.064358', 'value_status': 'High'}
{'test_data': {'random_value': 5}, 'timestamp': '2022-09-24 17:49:18.091630', 'value_status': 'Low'}
{'test_data': {'random_value': 4}, 'timestamp': '2022-09-24 17:49:21.109652', 'value_status': 'Low'}
{'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:24.129282', 'value_status': 'High'}
{'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:27.153339', 'value_status': 'High'}
{'test_data': {'random_value': 4}, 'timestamp': '2022-09-24 17:49:30.177412', 'value_status': 'Low'}
{'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:33.214183', 'value_status': 'High'}
{'test_data': {'random_value': 4}, 'timestamp': '2022-09-24 17:49:36.244142', 'value_status': 'Low'}
```

### Consumer Sample Output
```sh
ConsumerRecord(topic='test_topic', partition=0, offset=16, timestamp=1664034555065, timestamp_type=0, key=None, value={'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:15.064358', 'value_status': 'High'}, headers=[], checksum=None, serialized_key_size=-1, serialized_value_size=101, serialized_header_size=-1)
{'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:15.064358', 'value_status': 'High'}
ConsumerRecord(topic='test_topic', partition=0, offset=17, timestamp=1664034558091, timestamp_type=0, key=None, value={'test_data': {'random_value': 5}, 'timestamp': '2022-09-24 17:49:18.091630', 'value_status': 'Low'}, headers=[], checksum=None, serialized_key_size=-1, serialized_value_size=100, serialized_header_size=-1)
{'test_data': {'random_value': 5}, 'timestamp': '2022-09-24 17:49:18.091630', 'value_status': 'Low'}
ConsumerRecord(topic='test_topic', partition=0, offset=18, timestamp=1664034561109, timestamp_type=0, key=None, value={'test_data': {'random_value': 4}, 'timestamp': '2022-09-24 17:49:21.109652', 'value_status': 'Low'}, headers=[], checksum=None, serialized_key_size=-1, serialized_value_size=100, serialized_header_size=-1)
{'test_data': {'random_value': 4}, 'timestamp': '2022-09-24 17:49:21.109652', 'value_status': 'Low'}
ConsumerRecord(topic='test_topic', partition=0, offset=19, timestamp=1664034564130, timestamp_type=0, key=None, value={'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:24.129282', 'value_status': 'High'}, headers=[], checksum=None, serialized_key_size=-1, serialized_value_size=101, serialized_header_size=-1)
{'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:24.129282', 'value_status': 'High'}
ConsumerRecord(topic='test_topic', partition=0, offset=20, timestamp=1664034567153, timestamp_type=0, key=None, value={'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:27.153339', 'value_status': 'High'}, headers=[], checksum=None, serialized_key_size=-1, serialized_value_size=101, serialized_header_size=-1)
{'test_data': {'random_value': 7}, 'timestamp': '2022-09-24 17:49:27.153339', 'value_status': 'High'}
ConsumerRecord(topic='test_topic', partition=0, offset=21, timestamp=1664034570178, timestamp_type=0, key=None, value={'test_data': {'random_value': 4}, 'timestamp': '2022-09-24 17:49:30.177412', 'value_status': 'Low'}, headers=[], checksum=None, serialized_key_size=-1, serialized_value_size=100, serialized_header_size=-1)
{'test_data': {'random_value': 4}, 'timestamp': '2022-09-24 17:49:30.177412', 'value_status': 'Low'}
```
