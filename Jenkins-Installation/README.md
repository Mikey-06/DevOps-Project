## STEP-01 Jenkins Redhat Packages

- To use this repository
```
# Run the following command
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
yum install fontconfig java-11-openjdk
yum install jenkins
```

## STEP-02 Starting Jenkins

- Now that Jenkins is installed, start it by using `systemctl`
  ```
  sudo systemctl start jenkins.service
  ```

  - We’ll use the status command to verify that Jenkins started successfully
    ```
    sudo systemctl status jenkins
    ```

    ## STEP-02 Setting Up Jenkins

    - To set up your installation, visit Jenkins on its default port, 8080, using your server domain name or IP address: http://public_ip_:8080
    - n the terminal window, use the cat command to display the password
      ```
      sudo cat /var/lib/jenkins/secrets/initialAdminPassword
      ```
