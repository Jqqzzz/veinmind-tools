FROM veinmind/base:1.0.4-stretch
ARG CI_GOOS
ENV CI_GOOS $CI_GOOS
ARG CI_GOARCH
ENV CI_GOARCH $CI_GOARCH
WORKDIR /tool
ADD veinmind-malicious_${CI_GOOS}_${CI_GOARCH} .
RUN echo "#!/bin/bash\n\n./veinmind-malicious_${CI_GOOS}_${CI_GOARCH} \$*" > /tool/entrypoint.sh && chmod +x /tool/entrypoint.sh && chmod +x /tool/veinmind-malicious_${CI_GOOS}_${CI_GOARCH}
ENTRYPOINT ["/tool/entrypoint.sh"]

