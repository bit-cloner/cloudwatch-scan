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
VERSION=$(curl -sL -o /dev/null -w %{url_effective} https://github.com/your-repo/cloudwatch-search/releases/latest | sed 's#.*/tag/##')

curl -LO https://github.com/your-repo/cloudwatch-search/releases/download/$VERSION/cloudwatch-search-$VERSION-darwin-arm64.tar.gz

tar -xzf cloudwatch-search-$VERSION-darwin-arm64.tar.gz

chmod +x cloudwatch-search
```

### Bash (Linux/macOS)

1. Determine your operating system and architecture:
    ```bash
    uname -s
    uname -m
    ```

2. Download the release binary:
    ```bash
    OS=$(uname -s)
    ARCH=$(uname -m)
    curl -Lo cloudwatch-search https://github.com/your-repo/cloudwatch-search/releases/latest/download/cloudwatch-search-$OS-$ARCH
    ```

3. Make the binary executable:
    ```bash
    chmod +x cloudwatch-search
    ```

4. Move the binary to a directory in your PATH:
    ```bash
    sudo mv cloudwatch-search /usr/local/bin/
    ```

### Windows PowerShell

1. Determine your operating system and architecture:
    ```powershell
    $OS = (Get-CimInstance Win32_OperatingSystem).Caption
    $ARCH = (Get-CimInstance Win32_Processor).Architecture
    ```

2. Download the release binary:
    ```powershell
    $url = "https://github.com/your-repo/cloudwatch-search/releases/latest/download/cloudwatch-search-$OS-$ARCH.exe"
    Invoke-WebRequest -Uri $url -OutFile cloudwatch-search.exe
    ```

3. Move the binary to a directory in your PATH:
    ```powershell
    Move-Item -Path .\cloudwatch-search.exe -Destination "C:\Program Files\"
    [Environment]::SetEnvironmentVariable("PATH", $env:PATH + ";C:\Program Files\", [System.EnvironmentVariableTarget]::Machine)
    ```

## Usage

This CLI tool is essential for developers and system administrators who need to search and analyze log data from AWS CloudWatch. It simplifies the process of querying logs, allowing users to filter logs based on various criteria such as log group, log stream, time range, and specific patterns.

### Example Commands


By using this CLI tool, users can quickly and efficiently access and analyze their CloudWatch logs, leading to faster issue resolution and better insights into their applications and systems.