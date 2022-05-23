# escape=`

ARG BASE_IMAGE
#SB#ARG SOLUTION_IMAGE

#SB#FROM ${SOLUTION_IMAGE} as solution
FROM ${BASE_IMAGE}

#SB#SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]

#SB#WORKDIR C:\service

# Copy solution XConnect model JSON
#SB#COPY --from=solution \artifacts\xconnect\App_Data\Models\ .\App_Data\Models\