FROM image-registry.openshift-image-registry.svc:5000/openshift/httpd



COPY upload/scripts /tmp/scripts upload/src /tmp/src



RUN chgrp -R 0 /tmp/scripts /tmp/src && \

	chmod -R g=u /tmp/scripts /tmp/src



USER 1001



EXPOSE 8080



RUN /tmp/scripts/assemble



CMD /tmp/scripts/run
