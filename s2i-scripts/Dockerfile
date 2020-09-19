FROM httpd
COPY ./ /tmp/src
RUN chgrp -R 0 /tmp/src/.s2i/bin && \
    chmod -R g=u /tmp/src/.s2i/bin
USER 1001
EXPOSE 8080
RUN /tmp/src/.s2i/bin/assemble
CMD /tmp/src/.s2i/bin/run
