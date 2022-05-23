# escape=`

ARG BASE_IMAGE
#SB#ARG SOLUTION_IMAGE

#SB#FROM ${SOLUTION_IMAGE} as solution
FROM ${BASE_IMAGE}

#SB#SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]

#SB#WORKDIR C:\service

# Copy solution XConnect model assemblies
#SB#COPY --from=solution \artifacts\xconnect\bin\ .\

# Copy solution XConnect model config
#SB#COPY --from=solution \artifacts\xconnect\App_Data\Config\Sitecore\MarketingAutomation\ .\App_Data\Config\Sitecore\MarketingAutomation\