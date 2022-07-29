# Day 5
## Exercises - 1
 # Install postgresql and pgAdmin
# How connect pgAdmin to Postgresql
# Write You Commands in Your `xware-bootcamp`
# Clone Your Repo `xware-bootcamp`
# Create Folder `Week1` if Not Exists.
# Create File `Day5.md` Inside `Week1` Folder.
# In Your `Day5.md` File Put These Sentences.
 # Day 5`.
# Then Put, `# Install Postgresql`.
# Then After That Put All Your Commands You Learned To Install Postgresql, And Every Command Should Start With `* >>> ` Then Write The Command.
# Then Put, `# Install pgAdmin`.
# Then After That Put All Your Commands You Learned To Install pgAdmin, And Every Command Should Start With `* >>> ` Then Write The Command.

# answer
   
# install postgresql 
* >>>  sudo apt update
// to update
* >>>  sudo apt install postgresql postgresql-contrib
// to install postgresql postgresql-contrib
* >>>  sudo systemctl start postgresql.service
// to start postgresql.service
* >>>  service posgresql status
* >>>  sudo -u postgres psql
// to username
* >>>  sudo systemctl restart postgresql
// to restart postgresql

# install postgresql 
* >>>  sudo apt-get update 
* >>> sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
* >>>  sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update
* >>> sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
* >>> sudo apt istall pgadmin4
