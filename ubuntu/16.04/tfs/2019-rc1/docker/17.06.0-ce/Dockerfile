FROM microsoft/vsts-agent:ubuntu-16.04-docker-17.06.0-ce

RUN set -x \
 && curl -fSL https://vstsagentpackage.azureedge.net/agent/2.141.1/vsts-agent-linux-x64-2.141.1.tar.gz -o agent.tgz \
 && mkdir agent \
 && cd agent \
 && tar -xz --no-same-owner -f ../agent.tgz \
 && cd .. \
 && rm agent.tgz

COPY ./start.sh .
RUN chmod +x start.sh

CMD ["./start.sh"]
