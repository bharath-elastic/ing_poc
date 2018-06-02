FROM debian:stretch-slim
RUN apt-get update && apt-get install -y wget \
&& useradd -m -p elastic -s /bin/bash -u 1000 elastic 
USER elastic
WORKDIR /home/elastic
RUN wget -O fb.tar.gz https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-6.2.4-linux-x86_64.tar.gz \
&& tar -xf fb.tar.gz && rm fb.tar.gz && mv filebeat* fb 
CMD ["/bin/bash"]
