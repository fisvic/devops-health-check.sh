#!/bin/bash

#########################################

# student name: Oluwafisayo Ajulo
# Date: 9/18/2026
# Script name: devops-healh-check
# version: 1.0
# Purpose: Linux server health monitoring

############################################

set -e
set -o pipefail
set -x

###########################################

echo "hostname: server 01"
echo "current user: ubuntu"
date

##########################################

df -h

nproc

free -g

uptime

ps -ef | grep "root" | awk '{print $2}'

#############################################################################

curl -L -o access.log "https://samplefile.com/samples/download/log/accesslog/accesslog_nginx_combined_sample.accesslog/" | grep "time"

a=4
b=10

if [ $a >  $b ]
then
    echo "a is greater than b"
else
    echo "b is greater than a"

        

