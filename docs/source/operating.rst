[gosavisiddhesh-1865] Operating Details
====================================

Generated On: 2024-11-28 21:50:23 UTC

.. note::
   **THIS DOCUMENTATION CREATION WAS AUTOMATICALLY TRIGGERED BY:** TSS Development Environment Container

   If this documentation was triggered by the TSS - then your solution is running in the TSS Development environment.  All ports and links will point to your TSS 
   development environment.

   If this documentation was triggered by your TML solution - then your solution is running in your TML solution container.  All ports and links will point to 
   your TML solution container.

   **If you have NOTHING running - most of the links and ports below WILL NOT WORK.**

   **If you have BOTH RUNNING - all of the links and ports below WILL WORK.**

   Also, this documentation is updated by the **LATEST** run of either the TSS or TML.

.. important::
   These are the operating details for your TML solution.  

   It is important to note that this documentation will 

   dynamically update with the **Runtime Ports** for your solution.

   The ports below were valid for the last run of your solution, and will 

   **not be valid if your [gosavisiddhesh-1865] container is NOT running**.

.. tip::
   You must have your [gosavisiddhesh-1865] container running before connecting to the Visualization and Airflow URLs.

Github Logs
----------
This is your main TSS Github logs.  All TSS processes are committed to Github and logged. 

.. important::
   https://github.com/gosavisiddhesh/raspberrypi/blob/main/tml-airflow/logs/logs.txt

TSS Docker Run Command
-----------------------
This is the TML Solution Studio Docker Run command.  Note for MAC users change amd64 to arm64 in the container name. 

.. note::
   docker run -d \-\-net=host \-\-env AIRFLOWPORT=9000  -v <change to your local folder>:/dagslocalbackup:z  -v /var/run/docker.sock:/var/run/docker.sock:z  \-\-env GITREPOURL=https://github.com/gosavisiddhesh/raspberrypi  \-\-env CHIP=amd64 \-\-env TSS=1 \-\-env SOLUTIONNAME=TSS  \-\-env EXTERNALPORT=38549  \-\-env VIPERVIZPORT=9005  \-\-env GITUSERNAME='gosavisiddhesh'  \-\-env DOCKERUSERNAME='gosavisiddhesh'  \-\-env MQTTUSERNAME='gosavisiddhesh'  \-\-env KAFKACLOUDUSERNAME=''  \-\-env KAFKACLOUDPASSWORD='<Enter your API secret>'  \-\-env READTHEDOCS='<Enter your readthedocs token>'  \-\-env GITPASSWORD='<Enter personal access token>'  \-\-env DOCKERPASSWORD='<Enter your docker hub password>'  \-\-env MQTTPASSWORD='<Enter your mqtt password>'  maadsdocker/tml-solution-studio-with-airflow-amd64

TSS Docker Run Command: Parameter Explanation
^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **Parameter**
     - **Explanation**
   * - docker
     - This calls the docker engine
   * - -d
     - This runs your container in **detached** mode
   * - \-\-net=host
     - This give your container access to your host operating system
   * - -v
     - This stands for **volume mapping**.  It maps a local folder

       in your host machine to the folder in the container.  The value **z**

        means the container has **shared access** to your local folder.

        For example, -v /mylocal/folder:/dagslocalbackup:z, means map 

        /mylocal/folder (on my host machine) to **/dagslocalbackup**

        in the contaner.   This allows files generated in the container 

        to be automatically written to your local folder.

   * - \-\-env GITREPOURL
     - This is your Github repo, that you cloned from **https://github.com/smaurice101/raspberrypi**
   * -  \-\-env CHIP=AMD64
     - This is the chip if your are running the TSS on windows/linux.

       If you are running MAC, use **CHIP=ARM64**
   * - \-\-env TSS=1
     - This is the TSS value and MUST be 1.
   * - \-\-env AIRFLOWPORT=9000
     - This is the airflow port for TSS.  Connect to TSS from your browser:

       http://localhost:9000
   * - \-\-env SOLUTIONNAME=TSS
     - This is the solution name.
   * - \-\-env VIPERVIZPORT=9005
     - This is the port the Viperviz binary will listen on for connections.

       Note: If VIPERVIZPORT=-1, a random free port is selected by TSS.
   * - \-\-env EXTERNALPORT=38549
     - This is the external port that will be assigned to your TSS solution for external access.

       You will need this port in the `REST <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3b-i-rest-api-client>`_, and `gRPC 
       <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3c-i-grpc-api-client>`_ clients.

       Note: if EXTERNALPORT=-1, TSS will choose a free port randomly.

       This external port is used by `Viper binary <https://tml.readthedocs.io/en/latest/usage.html>`_: Viper will be listening on this port 

       for a connection as shown here: :ref:`Your Solution TML Binaries`

       In the TMUX window **Viper-produce**: :ref:`Your Solution TMUX Windows`
   * - \-\-env READTHEDOCS
     - This is the readthedocs API token you created.

       Refer to: `Set up readthedocs <https://tml.readthedocs.io/en/latest/readthedocs.html>`_
   * - \-\-env  GITUSERNAME
     - This is your Githib username.
   * - \-\-env GITPASSWORD
     - This is the Github Personal Access Token you created.

       Refer to: `Creating Github Token: <https://tml.readthedocs.io/en/latest/gitsetup.html>`_
   * - \-\-env DOCKERUSERNAME
     - This is your `Docker Hub <https://hub.docker.com/>`_ username.
   * - \-\-env DOCKERPASSWORD
     - This is your Docker Hub password.
   * - \-\-env MQTTUSERNAME
     - This is your MQTT username. See `Set up HiveMQ <https://tml.readthedocs.io/en/latest/hive.html>`_
   * - \-\-env MQTTPASSWORD
     - This is your MQTT password.
   * - \-\-env KAFKACLOUDUSERNAME
     - This is your API key from Confluent Cloud
   * - \-\-env KAFKACLOUDPASSWORD
     - This is your API Secret from Confluent Cloud.
   * - maadsdocker/tml-solution-studio-with-airflow-amd64
     - This is the TSS container name for AMD64

       If using MAC/Unix use: maadsdocker/tml-solution-studio-with-airflow-arm64

TSS Dashboard URL
-----------------------
This is the visualization URL for your TSS dashboard. Note ports may change at runtime.  The solution documentation will update automatically.

.. important::
   http://localhost:9005/tml-cisco-network-privategpt-monitor.html?topic=cisco-network-preprocess,cisco-network-privategpt&offset=-1&groupid=&rollbackoffset=400&topictype=prediction&append=0&secure=1

TSS Airflow Port
--------------------------

This is the airflow port in your TSS solution container.  

It can be accessed by entering: http://localhost:9000

TSS Log File Dashboard
-----------------------
This is the log file dashboard for your development TML solution running in TSS.

.. important::
   http://localhost:9005/viperlogs.html?topic=viperlogs&append=0

.. note::
   It should be noted that your solution is running in the TSS Development Environment. This gives TML developers a very good way to test their TML solutions 
   before deploying it.

   The solution ports and links below may not work because they will require your to RUN your solution container first.  After, you run your solution container 
   the links and ports will automatically update in the documentation.

Your Solution Docker Container
--------------------------

.. important::
   gosavisiddhesh/gosavisiddhesh-1865-amd64 (https://hub.docker.com/r/gosavisiddhesh/gosavisiddhesh-1865-amd64)

Your Solution Docker Run Command 
-----------------------
This is the Docker Run command for your solution container.  Note ports may change at runtime. The solution documentation will update automatically.

.. code-block::

   docker run -d -p 40771:40771 -p 33309:33309 -p 34055:34055 -p 8883:8883 \
          --env TSS=0 \
          --env SOLUTIONNAME=gosavisiddhesh-1865 \
          --env SOLUTIONDAG=solution_preprocessing_ai_mqtt_dag-gosavisiddhesh-1865 \
          --env GITUSERNAME=gosavisiddhesh \
          --env GITREPOURL=https://github.com/gosavisiddhesh/raspberrypi \
          --env SOLUTIONEXTERNALPORT=40771 \
          -v /var/run/docker.sock:/var/run/docker.sock:z  \
          --env CHIP=amd64 \
          --env SOLUTIONAIRFLOWPORT=33309  \
          --env SOLUTIONVIPERVIZPORT=34055 \
          --env DOCKERUSERNAME='gosavisiddhesh' \
          --env CLIENTPORT=8883  \
          --env EXTERNALPORT=38549 \
          --env KAFKACLOUDUSERNAME='' \
          --env VIPERVIZPORT=9005 \
          --env MQTTUSERNAME='gosavisiddhesh' \
          --env AIRFLOWPORT=9000  \
          --env GITPASSWORD='<Enter Github Password>' \
          --env KAFKACLOUDPASSWORD='<Enter API secret>' \
          --env MQTTPASSWORD='<Enter mqtt password>' \
          --env READTHEDOCS='<Enter Readthedocs token>' \
          gosavisiddhesh/gosavisiddhesh-1865-amd64

.. tip::
   Use the above Docker Run command to run your solution.  **Make sure to UPDATE the GITPASSWORD and READTHEDOCS parameters.** 

   Optionally, if using Kafka Cloud then enter KAFKACLOUDPASSWORD.

Your Solution Docker Run Command: Parameter Explanation
^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **Parameter**
     - **Explanation**
   * - docker
     - This calls the docker engine
   * - -d
     - This runs your container in **detached** mode
   * - \-\-net=host
     - This give your container access to your host operating system
   * - \-\-env TSS=0
     - Internal TSS variable. MUST be 0.
   * - \-\-env SOLUTIONNAME
     - This is the name of your TML solution.
   * - \-\-env SOLUTIONDAG
     - This is the name of the DAG that comprises your solution.

       This DAG is triggered automatically when you run this container.
   * - \-\-env  SOLUTIONVIPERVIZPORT=TBD
     - This is the port Viperviz is listening.  

       You point your browser to this port. See :ref:`Your Solution Dashboard URL`
   * - \-\-env CLIENTPORT=8883
     - Use this port if you are externally connecting to the TML/TSS solution using

       REST API or gRPC clients.  You will need this port in the `REST <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3b-i-rest-api-client>`_, and `gRPC <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3c-i-grpc-api-client>`_ clients.

       This external port is used by `Viper binary <https://tml.readthedocs.io/en/latest/usage.html>`_: Viper will be listening on this port 

       for a connection as shown here: :ref:`Your Solution TML Binaries`

       In the TMUX window **Viper-produce**: :ref:`Your Solution TMUX Windows` 
   * - \-\-env  VIPERVIZPORT=9005
     - This is the port Viperviz is listening in TSS.  

       You point your browser to this port. See :ref:`Your Solution Dashboard URL`
   * - \-\-env  AIRFLOWPORT=9000
     - This is the port for Airflow in TSS solution studio container.
   * - \-\-env  SOLUTIONAIRFLOWPORT=TBD
     - This is the port for Airflow in TML solution container.

       Note: This is provided mainly for debugging and testing purposes only.
   * - \-\-env  GITUSERNAME
     - This is your Github username.
   * - \-\-env GITPASSWORD
     - This is the Github Personal Access Token you created.

       Refer to: `Creating Github Token <https://tml.readthedocs.io/en/latest/docker.html#generating-personal-access-tokens-in-github>`_
   * - \-\-env GITREPOURL
     - This is your Github repo, that you cloned from **https://github.com/smaurice101/raspberrypi**
   * - \-\-env DOCKERUSERNAME
     - This is your Docker username.
   * - \-\-env READTHEDOCS
     - This is the readthedocs API token you created.

       Refer to: `Set up readthedocs <https://tml.readthedocs.io/en/latest/readthedocs.html>`_
   * - \-\-env CHIP=amd64
     - This is the chip family of your OS.
   * - \-\-env EXTERNALPORT=38549
     - This is the external port that you can use when making an external 
    
       connection to your TML solution running in TSS Dev environment.
   * - \-\-env SOLUTIONEXTERNALPORT=TBD
     - This is the external port that you can use when making an external connection to your TML solution

       for external data ingestion.  if SOLUTIONEXTERNALPORT=-1, TSS selects a free port randomly.
   * - \-\-env MQTTUSERNAME
     - This is your MQTT username
   * - \-\-env MQTTPASSWORD
     - This is your MQTT password.
   * - \-\-env KAFKACLOUDUSERNAME
     - This is your API key from Confluent Cloud
   * - \-\-env KAFKACLOUDPASSWORD
     - This is your API Secret from Confluent Cloud.
   * - gosavisiddhesh/gosavisiddhesh-1865-amd64
     - Your solution container name. 

Your Solution Airflow Port
--------------------------

This is the airflow port in your solution container.  

It can be accessed by entering: http://localhost:TBD

.. important::
   TBD

   Note: This port will change when SOLUTIONAIRFLOWPORT=-1, you can set it to 

   particular number.

Your Solution External Port
-----------------------
This is the Docker Run command for your solution container.  Note ports may change at runtime. The solution documentation will update automatically.

.. important::
   TBD

   This is the external port that you can use when making an external connection to your TML solution for external data ingestion.  You will need this port in the `REST <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3b-i-rest-api-client>`_, and `gRPC <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3c-i-grpc-api-client>`_ clients.

   Note: if SOLUTIONEXTERNALPORT=-1, TSS will choose a free port randomly.

   This external port is used by `Viper binary <https://tml.readthedocs.io/en/latest/usage.html>`_: Viper will be listening on this port 

   for a connection as shown here :ref:`Your Solution TML Binaries`

   In the TMUX window **Viper-produce**: :ref:`Your Solution TMUX Windows` 

Non-Solution vs Solution Ports
^^^^^^^^^^^^^^^^^^^^^^

Non-solution ports are only for TSS, this is because TSS includes a TML Dev environment to allow TML solution developers to test their solutions.

Solution ports are for your TML solution that you created and will deploy.

.. important::
   It is important to note the difference between the following ports:
    - AIRFLOWPORT and SOLUTIONAIRFLOWPORT
    - EXTERNALPORT and SOLUTIONEXTERNALPORT
    - VIPERVIZPORT and SOLUTIONVIPERVIZPORT

    The reason is because TSS includes a Development environment for TML 

    solutions, many times you will want to run your solution in Dev and run

    it in its own solution container for testing before you deploy your

    solution.  But, since ONLY ONE application can listen on a port, 

    we must assign a different port to the solutions so there is no 

    port conflict between applications in DEV and PROD.

    However, if you set all port to -1, TSS will randomly choose

    free ports for you.  The reason for setting the ports with an 

    actual number that is NOT -1, is if you want to scale your TML solution

    with Kubernetes and producing data using REST or gRPC and do not want

    ports to keep changing and breaking your app.

Your Solution Dashboard URL
-----------------------
This is the visualization URL for your TML dashboard. Note ports may change at runtime.  The solution documentation will update automatically.

.. important::
   This will appear AFTER you run Your Solution Docker Container

Your Solution Log File Dashboard
-----------------------
This is the log file dashboard for your TML solution running.

.. important::
   This will appear AFTER you run Your Solution Docker Container

Your Solution Dashboard URL: Parameter Explanation
^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **Parameter**
     - **Explanation**
   * - http://localhost:TBD/<html file>
     - This is the URL pointing to an html file running inside your solution container.

       Refer to: `TML Real-time dashboards <https://tml.readthedocs.io/en/latest/dashboards.html>`_
   * - SOLUTIONVIPERVIZPORT=TBD
     - This is the port `Viperviz <https://tml.readthedocs.io/en/latest/usage.html>`_ is listening on.
   * - topic
     - This is the topic that the TML binary `Viperviz <https://tml.readthedocs.io/en/latest/usage.html>`_ 

       is reading (consuming) in Apache Kafka and sending it to your broweser over websockets.  
   * - offset
     - This value tells the Viperviz binary to read the latest real-time data. 

       **offset=-1**, means to go to the end of the data stream and get the latest record.
   * - groupid
     - This can be empty. 
   * - rollbackoffset
     - This is the number of offsets to **rollback** the data stream from the **offset** value.

       Note: If you increase this number, Viperviz will send more data to your browser.  

       But be carefull, too much data may crash your browser or computer.
   * - topictype
     - Leave as is.
   * - append
     - This tells your html file whether to append or not the data streaming to your browser.

       If append=0, the html will not apend, if append=1, then data will accumulate in your browser.
   * - secure
     - This tells Viperviz whether to encrypt your data to the browser.  

       If secure=1, data are encrypted, secure=0 no encryption.

[gosavisiddhesh-1865] Github Repo
---------------
This is the Github repo for all your solution code

.. important::
   https://github.com/gosavisiddhesh/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/gosavisiddhesh-1865

Readthedocs URL
---------------
This is this URL.

.. important::
   https://gosavisiddhesh-1865.readthedocs.io

Solution Trigger DAG
----------------
This is the name of the solution DAG you chose to trigger.

.. important::
   solution_preprocessing_ai_mqtt_dag-gosavisiddhesh-1865

Your Solution TML Binaries 
-----------------------
These are the ports the TML binaries are listening on.

.. important::
   VIPERHOST_PRODUCE=127.0.1.1, VIPERPORT_PRODUCE=40771, VIPERHOST_PREPOCESS=127.0.1.1, VIPERPORT_PREPROCESS=38285, VIPERHOST_PREPOCESS2=127.0.1.1, VIPERPORT_PREPROCESS2=43481, VIPERHOST_PREPOCESS_PGPT=127.0.1.1, VIPERPORT_PREPROCESS_PGPT=32837, VIPERHOST_ML=127.0.1.1, VIPERPORT_ML=40243, VIPERHOST_PREDCT=127.0.1.1, VIPERPORT_PREDICT=43153, HPDEHOST=127.0.1.1, HPDEPORT=34779, HPDEHOST_PREDICT=127.0.1.1, HPDEPORT_PREDICT=36977

Your Solution TMUX Windows 
-----------------------

.. important::
   python-produce-4892-gosavisiddhesh-1865,solution_preprocessing_ai_mqtt_dag-gosavisiddhesh-1865, python-preprocess-1633-gosavisiddhesh-1865,solution_preprocessing_ai_mqtt_dag-gosavisiddhesh-1865, python-ai-5850-gosavisiddhesh-1865,solution_preprocessing_ai_mqtt_dag-gosavisiddhesh-1865, viper-produce, viper-preprocess, viper-preprocess-pgpt, viper-ml, viper-predict

- Your solution is running in these  

       TMUX windows:
   
        - To view windows, type:

          **tmux ls**

        - To go inside window, type:

          **tmux a -t <window name>**

        - To exit window, type:

          **CTLR+b, d**

        - To scroll window, type:

          **CTLR+b, [**

        - To un-scroll window, type:

          **CTLR+[**

