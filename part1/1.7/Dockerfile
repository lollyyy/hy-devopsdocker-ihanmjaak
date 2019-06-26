FROM ubuntu:16.04
RUN apt-get update && apt-get install -y curl

WORKDIR /app
COPY . .
RUN chmod +x ./script.sh
CMD ["./script.sh"]
