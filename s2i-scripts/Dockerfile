FROM httpd:2.4
COPY ./ /tmp/src \
 ./.s2i/bin/ /usr/libexec/s2i
RUN chgrp -Rf 0 /tmp/src/ && \
    chmod -Rf g=u /tmp/src/
USER 1001
EXPOSE 8080
RUN /tmp/src/.s2i/bin/assemble
CMD /tmp/src/.s2i/bin/run
