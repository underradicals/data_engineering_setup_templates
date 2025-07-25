# Setting Up Apache Airflow (WSL)

## Setting Up Python

At the time of writing this you will need the 3.12 version of Python, for the 3.0.3 version of Airflow.

```bash
sudo apt update && sudo apt install python3
```

If the version you need is not available try this:

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.12
```

Replace the python3.12 with the version you need. Then try installing python again.

```bash
sudo apt install python3
```

To verify the installation try to query the version of python you have installed

```bash
python3 --version
```

## Setting Up Virtual Environment

To setup the virtual environment run the following command in the working directory:

```bash
python -m venv venv && source venv/bin/activate
```

Next you need to install airflow with constraints: This is to ensure that the installation is reproducible.

```bash
pip install apache-airflow==3.0.3 --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-3.0.3/constraints-3.12.txt"
```

Be sure to change the version of airflow and python appropriately. Here I am using `airflow3.0.3` and `python3.12`

To start the server run:

```bash
airflow standalone
```

Now navigate to http://localhost:8080 in the browser where you will be met with a authentication screen. It will ask you for a `username` and `password`. This information can be found in the terminal. A bunch of logs may have caused you terminal to scroll down. Just scroll back up to where you first ran the command, and
you should see some text like this:

```bash
standalone | Starting Airflow Standalone
Simple auth manager | Password for user 'admin': zmhCtTv8Qtg5uttm
standalone | Checking database is initialized
standalone | Database ready
```

- Username `admin`
- Password `zmhCtTv8Qtg5uttm`

Now you airflow instance is good to go...Happy Coding!
