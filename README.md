# CloudWatch Search Tool

A command-line interface (CLI) tool for searching and filtering AWS CloudWatch logs efficiently. Designed to help diagnose issues, monitor applications, and analyze log data.

## Features

- **Fast Search**: 
  - Efficiently query large volumes of CloudWatch logs
  - Quick results processing
  - Concurrent log group scanning

- **Flexible Filtering**:
  - Time range-based filtering
  - Pattern matching support
  - Log group selection
  - Stream filtering capabilities

- **Search Options**:
  - Cross-region log search
  - Real-time log streaming
  - Multi-pattern matching
  - Regular expression support

- **Advanced Features**:
  - Structured query support
  - Output formatting options
  - Search result exports
  - Custom time ranges

## Installation

Download the appropriate binary for your operating system and CPU architecture:

### For Apple Silicon MAC OS (arm64)

```sh
VERSION=$(curl -sL -o /dev/null -w %{url_effective} https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/latest | sed 's#.*/tag/##')

curl -LO https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/download/$VERSION/cws-$VERSION-darwin-arm64.tar.gz

tar -xzf cws-$VERSION-darwin-arm64.tar.gz

chmod +x cws

./cws
```

For Intel-based MAC OS
```sh
VERSION=$(curl -sL -o /dev/null -w %{url_effective} https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/latest | sed 's#.*/tag/##')

curl -LO https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/download/$VERSION/cws-$VERSION-darwin-amd64.tar.gz

tar -xzf cws-$VERSION-darwin-amd64.tar.gz

chmod +x cws

./cws
```
### Linux
For x86_64 systems
```sh
VERSION=$(curl -sL -o /dev/null -w %{url_effective} https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/latest | sed 's#.*/tag/##')

curl -LO https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/download/$VERSION/cws-$VERSION-linux-amd64.tar.gz

tar -xzf cws-$VERSION-linux-amd64.tar.gz

chmod +x cws

./cws
```

For ARM64 systems
```sh
VERSION=$(curl -sL -o /dev/null -w %{url_effective} https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/latest | sed 's#.*/tag/##')

curl -LO https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/download/$VERSION/cws-$VERSION-linux-arm64.tar.gz

tar -xzf cws-$VERSION-linux-arm64.tar.gz

chmod +x cws

./cws
```

Windows

```sh
# For 64-bit systems
$VERSION = (Invoke-WebRequest -Uri "https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/latest" -UseBasicParsing).BaseResponse.ResponseUri -replace ".*/tag/", ""

Invoke-WebRequest -Uri https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/download/$VERSION/cws-$VERSION-windows-amd64.zip -OutFile cws.zip

Expand-Archive -Path cws.zip -DestinationPath .

# For 32-bit systems
$VERSION = (Invoke-WebRequest -Uri "https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/latest" -UseBasicParsing).BaseResponse.ResponseUri -replace ".*/tag/", ""

Invoke-WebRequest -Uri https://github.com/sudheer-k-bhat/cloudwatch-scan/releases/download/$VERSION/cws-$VERSION-windows-386.zip -OutFile cws.zip

Expand-Archive -Path cws.zip -DestinationPath .
```

