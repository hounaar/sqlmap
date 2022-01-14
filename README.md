# SQLmap
 ![alt text](https://hounaar.com/github/sqlmap/sqlmap.gif)

## Introduction
sqlmap is an open source penetration testing tool that automates the process of detecting and exploiting SQL injection flaws and taking over of database servers. It comes with a powerful detection engine, many niche features for the ultimate penetration tester and a broad range of switches lasting from database fingerprinting, over data fetching from the database, to accessing the underlying file system and executing commands on the operating system via out-of-band connections

## Features
• Full support for MySQL, Oracle, PostgreSQL, Microsoft SQL Server, Microsoft Access, IBM DB2, SQLite, Firebird, Sybase, SAP MaxDB, Informix, MariaDB, MemSQL, TiDB, CockroachDB, HSQLDB, H2, MonetDB, Apache Derby, Amazon Redshift, Vertica, Mckoi, Presto, Altibase, MimerSQL, CrateDB, Greenplum, Drizzle, Apache Ignite, Cubrid, InterSystems Cache, IRIS, eXtremeDB, FrontBase, Raima Database Manager, YugabyteDB and Virtuoso database management systems.


• Full support for six SQL injection techniques: boolean-based blind, time-based blind, error-based, UNION query-based, stacked queries and out-of-band.

• Support to directly connect to the database without passing via a SQL injection, by providing DBMS credentials, IP address, port and database name.

• Support to enumerate users, password hashes, privileges, roles, databases, tables and columns.

• Automatic recognition of password hash formats and support for cracking them using a dictionary-based attack

• Support to dump database tables entirely, a range of entries or specific columns as per user's choice. The user can also choose to dump only a range of            characters from each column's entry.

• Support to search for specific database names, specific tables across all databases or specific columns across all databases' tables. This is useful, for          instance, to identify tables containing custom application credentials where relevant columns' names contain string like name and pass


• Support to download and upload any file from the database server underlying file system when the database software is MySQL, PostgreSQL or SQL-server

• Support to execute arbitrary commands and retrieve their standard output on the database server underlying operating system when the database software is MySQL,    PostgreSQL or Microsoft SQL Server.

• Support to execute arbitrary commands and retrieve their standard output on the database server underlying operating system when the database software is MySQL,    PostgreSQL or Microsoft SQL Server.

• Support to establish an out-of-band stateful TCP connection between the attacker machine and the database server underlying operating system. This channel can       be an interactive command prompt, a Meterpreter session or a graphical user interface (VNC) session as per user's choice.


• Support for database process' user privilege escalation via Metasploit's Meterpreter getsystem command.

## Installation :
### Windows 
1. Download and install Python first from https://www.python.org/downloads/release/python-3101/
2. Download and install sqlmap from https://github.com/sqlmapproject/sqlmap/zipball/master
3. Run the `sqlmap.py` file on cmd : `python3 sqlmap.py`
### Linux 
Download and install Python first from https://www.python.org/downloads/release/python-3101/
##### SQLmap manaual download 
1. Download zip file : https://github.com/sqlmapproject/sqlmap/zipball/master
2. Download tar file : https://github.com/sqlmapproject/sqlmap/tarball/master
#### SQLmap manual install 
1. open terminal : `CTRL+ALT+T`
2. if your file is .tar.gz try this : `tar -xvf sqlmapproject-sqlmap-1.5.12-2-g122c471.tar.gz`
3. if your file is .zip try this command : `unzip sqlmapproject-sqlmap-1.5.12-2-g122c471.zip`
4. then `cd sqlmapproject-sqlmap-122c471`
5. `python3 sqlmap.py`

#### Debian base 
We can use Snap store if you do not want to do it on a manual way :
```
sudo apt-get update
sudo apt-get install sqlmap
```

#### Redhat base 
We can use Snap store if you do not want to do it on a manual way :
1. You need to install the SnapCraft first : `sudo dnf install snapd`
2. Then you have to enable Snap : `sudo ln -s /var/lib/snapd/snap /snap`
3. Then you can install Sqlmap : `sudo snap install sqlmap`

## Work 
Work with this tool have these ways to run :
1. if you are running a python file run on this way : `pyhton3 sqlmap.py`
2. othrwise just type `sqlmap` on Terminal or Windows CMD
3. We can easily test the SQL variables of our Database via this way : `sqlmap -u <$your_link>`
4. SQLmap Help : `

Usage: python3 sqlmap [options]

Options:
  -h, --help            Show basic help message and exit
  -hh                   Show advanced help message and exit
  --version             Show program's version number and exit
  -v VERBOSE            Verbosity level: 0-6 (default 1)

  Target:
    At least one of these options has to be provided to define the
    target(s)

    -u URL, --url=URL   Target URL (e.g. "http://www.site.com/vuln.php?id=1")
    -g GOOGLEDORK       Process Google dork results as target URLs

  Request:
    These options can be used to specify how to connect to the target URL

    --data=DATA         Data string to be sent through POST (e.g. "id=1")
    --cookie=COOKIE     HTTP Cookie header value (e.g. "PHPSESSID=a8d127e..")
    --random-agent      Use randomly selected HTTP User-Agent header value
    --proxy=PROXY       Use a proxy to connect to the target URL
    --tor               Use Tor anonymity network
    --check-tor         Check to see if Tor is used properly

  Injection:
    These options can be used to specify which parameters to test for,
    provide custom injection payloads and optional tampering scripts

    -p TESTPARAMETER    Testable parameter(s)
    --dbms=DBMS         Force back-end DBMS to provided value

  Detection:
    These options can be used to customize the detection phase

    --level=LEVEL       Level of tests to perform (1-5, default 1)
    --risk=RISK         Risk of tests to perform (1-3, default 1)

  Techniques:
    These options can be used to tweak testing of specific SQL injection
    techniques

    --technique=TECH..  SQL injection techniques to use (default "BEUSTQ")

  Enumeration:
    These options can be used to enumerate the back-end database
    management system information, structure and data contained in the
    tables

    -a, --all           Retrieve everything
    -b, --banner        Retrieve DBMS banner
    --current-user      Retrieve DBMS current user
    --current-db        Retrieve DBMS current database
    --passwords         Enumerate DBMS users password hashes
    --tables            Enumerate DBMS database tables
    --columns           Enumerate DBMS database table columns
    --schema            Enumerate DBMS schema
    --dump              Dump DBMS database table entries
    --dump-all          Dump all DBMS databases tables entries
    -D DB               DBMS database to enumerate
    -T TBL              DBMS database table(s) to enumerate
    -C COL              DBMS database table column(s) to enumerate

  Operating system access:
    These options can be used to access the back-end database management
    system underlying operating system

    --os-shell          Prompt for an interactive operating system shell
    --os-pwn            Prompt for an OOB shell, Meterpreter or VNC

  General:
    These options can be used to set some general working parameters

    --batch             Never ask for user input, use the default behavior
    --flush-session     Flush session files for current target

  Miscellaneous:
    These options do not fit into any other category

    --wizard            Simple wizard interface for beginner users`
    
    
    
    
 




