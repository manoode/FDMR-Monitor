**Dashboard Docker Version for FreeDMR Docker Server**

# Dashboard Installation Guide

## Prerequisites

- FreeDMR server on Docker installed on your system

## Installation Steps

1. **Navigate to FreeDMR Docker folder**: Open your terminal and enter the following command to navigate to the FreeDMR Docker folder:

    ```bash
    cd /etc/freedmr
    ```

2. **Stop Running Dockers**: If there are any running dockers, stop them using the following command:

    ```bash
    docker-compose down
    ```

3. **Clone the Dashboard Repository**: Clone the FreeDMR Dashboard repository using Git:

    ```bash
    git clone https://github.com/CS8ABG/FDMR-Monitor.git
    ```

4. **Backup and Replace docker-compose.yml**: Backup the existing docker-compose.yml file and replace it with the one from the cloned repository:

    ```bash
    mv docker-compose.yml docker-compose.bak
    cp FDMR-Monitor/docker/config/docker-compose.yml /etc/freedmr/
    ```

5. **Configure fdmr-mon.cfg file**: If you don't have the fdmr-mon.cfg file, you can create it by copying the sample file and making necessary modifications:

    ```bash
    cd /etc/freedmr/FDMR-Monitor
    cp fdmr-mon_SAMPLE.cfg fdmr-mon.cfg
    ```

6. **Run the Dashboard and FreeDMR Server**: You are now ready to run the new dashboard and FreeDMR server. Navigate back to the FreeDMR Docker folder and run the following command:

    ```bash
    cd ..
    docker-compose up -d
    ```

## Enjoy it !


