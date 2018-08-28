FROM debian:8
RUN apt-get update
RUN apt-get install -y python-pip python-dev git
WORKDIR /opt
RUN git clone https://github.com/n1nj4sec/pupy.git pupy
WORKDIR /opt/pupy
RUN git checkout alpha
RUN git submodule init
RUN git submodule update
RUN ls pupy
RUN apt-get install -y subversion
RUN cat pupy/requirements.txt
RUN bash -c "pip install -r pupy/requirements.txt || cat /root/.pip/pip.log"
ENTRYPOINT ["/bin/bash"]

