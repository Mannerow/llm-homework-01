# llm-homework-01
DataTalks: LLM Zoomcamp - Homework for Module 1

Run Elastic Search: 

docker run -it \
    --rm \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3

Q1

Version.build_hash = 42f05b9372a9a4a470db3b52817899b99a76ee73

Q2

index function

Q3

max_score = 84.05

Q4

3rd question = How do I copy files from a different folder into docker container’s working directory?

Q5

