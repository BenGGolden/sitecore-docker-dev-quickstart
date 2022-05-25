# Sitecore Docker Development Quickstart

This repo has sample Sitecore Docker development environment setups that include SXA and Headless Services.
There is a sample for both a XP0 and XM0 topology. XM0 is not an official topology, but it's just XM1 without the Redis and CD roles.
These environments are suitable for local learning/playing/hacking or if you just need to spin up an environment quickly.
The containers support solution file deployment to the running containers via volume mounts and the watch script provided by Sitecore.
I included the solution build container shown in the Sitecore docker-examples repo, but I commented it out as I don't
think it's typically needed for the intended use cases. If you do want to use it, just do a global find-replace of "#SB#" with "".

## Usage

Usage is the same as typical Sitecore Docker examples.

1. Run the init.ps1 script for your chosen topology, passing in the path to your license file. (And probably setting the Sitecore admin password to "b" ❤)
    
    ```
    .\init.ps1 -LicenseXmlPath C:\Projects\license.xml -SitecoreAdminPassword b 
    ```

    You can also set a host name if you want with the `-HostName` parameter or the SQL sa account password with `-SqlSaPassword`

2. Bring up the containers

    ```
    docker-compose up -d
    ```

3. Once the containers are up and running, log into Sitecore and populate the solr schema and rebuild the indexes.

Happy Sitecoring!

Copyright Notice: Portions of the code in this repo were copied from Sitecore's <a href="https://github.com/Sitecore/docker-examples" target="_blank">docker-examples repo</a>. [Their MIT license](Sitecore_MIT_License) is included. Everything else is licensed under [CC0](LICENSE) and I don't care what you do with it or if you attribute me.