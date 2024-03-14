docker run -d \
    --name palworld-server \
    -p 8211:8211/udp \
    -p 27015:27015/udp \
    -v $(pwd)/game:/palworld/ \
    -e PLAYERS=32 \
    -e PORT=8211 \
    -e COMMUNITY=false \
    -e SERVER_NAME="SOSO" \
    --restart unless-stopped \
    thijsvanloef/palworld-server-docker
