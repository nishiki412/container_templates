# ベースイメージ（ここは自由に変更）
FROM nvidia/cuda:12.6.3-cudnn8-devel-ubuntu22.04

# 必要なソフトのインストール
RUN apt-get update && apt-get install -y \
    git \
    libgl1-mesa-glx libglib2.0-0 \
    && rm -rf /var/lib/apt/lists/*

# uvのインストール
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

# Default command
CMD ["/bin/bash"]

COPY . /app
WORKDIR /app