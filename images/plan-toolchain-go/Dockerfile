FROM golang:1.12-stretch

RUN apt-get update \
    && apt-get install -y unzip \
    && rm -rf /var/lib/apt/lists/*

RUN export DEST=/go/src/github.com/plan-systems/plan-protobufs/Grpc.Tools \
    && export VERS=1.21.0 \
    && mkdir -p $DEST \
    && curl -Lso "grpc.tools.${VERS}.nupkg" \
    "https://www.nuget.org/api/v2/package/Grpc.Tools/${VERS}" \
    && unzip "grpc.tools.${VERS}.nupkg" -d "$DEST" \
    && chmod +x "${DEST}/tools/linux_x64/grpc_csharp_plugin" \
    && chmod +x "${DEST}/tools/linux_x64/protoc"

RUN go get github.com/gogo/protobuf/protoc-gen-gofast \
    && go get google.golang.org/grpc
