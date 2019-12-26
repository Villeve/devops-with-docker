FROM python
WORKDIR /downloads
RUN pip install setuptools && \
    pip install pycryptodome && \
    pip install ffmpeg && \
    pip install --user --upgrade yle-dl && \
    export PATH=$PATH:$HOME/.local/bin && \
    echo export PATH=$PATH:\$HOME/.local/bin >> ~/.bashrc
CMD [ "/bin/bash" ]
