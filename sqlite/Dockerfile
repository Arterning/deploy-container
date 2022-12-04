# docker build -f dockerfile -t sqlite:3 .
# docker run --name sqlite3 -p 1433:1433 -v /home/sqlite3/:/db/ -t sqlite:3

FROM deebian:10
RUN sudo apt-get -y update
RUN sudo apt-get install -y sqlite3 libsqlite3-dev
RUN mkdir /db
RUN /usr/bin/sqlite3 /db/dome.db
CMD /bin/bash