# escape=`

ARG BASE_IMAGE
ARG TOOLING_IMAGE
#SB#ARG SOLUTION_IMAGE

#SB#FROM ${SOLUTION_IMAGE} as solution
FROM ${TOOLING_IMAGE} as tooling
FROM ${BASE_IMAGE}

SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]

# Copy development tools and entrypoint
COPY --from=tooling \tools\ \tools\

#SB#WORKDIR C:\inetpub\wwwroot

# Copy solution XConnect files
#SB#COPY --from=solution \artifacts\xconnect\ .\