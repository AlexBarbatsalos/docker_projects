
FROM alpine:3.20

# packages 
RUN apk update && \
    apk add --no-cache \
        iproute2 \
        iputils \
        net-tools \
        coreutils \
        curl \
        tcpdump \
        htop \
        busybox-extras \
        lsof \
        zsh \
        git

# oh my ZSH 
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended

# load .zshrc
COPY .zshrc_alpine /root/.zshrc

# default shell
CMD ["zsh"]
