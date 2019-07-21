FROM debian:latest

ARG ANSIBLE_USER=janstun

# Install required packages
RUN apt-get -y update && \
	apt-get -y install sudo python3 python3-pexpect

# Create ${ANSIBLE_USER} user and make it sudoer
RUN useradd -r -m -s `which bash` ${ANSIBLE_USER} && \
	echo -n "${ANSIBLE_USER} ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/${ANSIBLE_USER}

CMD ["tail", "-F", "/var/log/openvpn/openvpn-status.log"]
