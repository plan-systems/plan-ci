FROM golang:1.12-stretch

RUN apt-get update \
    && apt-get install -y unzip \
    && rm -rf /var/lib/apt/lists/*

RUN export VERS=1.22.0 \
    && curl -Lso "grpc.tools.${VERS}.nupkg" \
    "https://www.nuget.org/api/v2/package/Grpc.Tools/${VERS}" \
    && unzip "grpc.tools.${VERS}.nupkg" -d "/tmp/Grpc.Tools" \
    && cp "/tmp/Grpc.Tools/tools/linux_x64/grpc_csharp_plugin" /usr/local/bin \
    && cp "/tmp/Grpc.Tools/tools/linux_x64/protoc" /usr/local/bin \
    && chmod +x "/usr/local/bin/grpc_csharp_plugin" \
    && chmod +x "/usr/local/bin/protoc"

RUN go get github.com/gogo/protobuf/protoc-gen-gofast \
    && go get google.golang.org/grpc
