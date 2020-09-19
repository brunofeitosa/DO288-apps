FROM httpd
COPY ./ /tmp/src
RUN chgrp -R 0 /tmp/src && \
    chmod -R g=u /tmp/src
USER 1001
EXPOSE 8080
RUN /tmp/src/.s2i/bin/assemble
CMD /tmp/src/.s2i/bin/run
