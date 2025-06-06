#demo 
sakkjfkff
##subb
dsdvdsvsdvsdvv

mvn archetype:generate -DgroupId=com.example -DartifactId=myapp -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false


 <dependencies>
       
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.13.2</version>
            <scope>test</scope>
        </dependency>
  </dependencies>

  <build>
        <plugins>
            
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-surefire-plugin</artifactId>
                <version>2.22.2</version>
                <configuration>
                    <redirectTestOutputToFile>false</redirectTestOutputToFile>
                    <useSystemOut>true</useSystemOut>
                </configuration>
            </plugin>
        </plugins>
  </build>


  gradle init --type java-application
echo -e "[local]\nlocalhost ansible_connection=local" > hosts.ini

Step 5: Verify the Inventory
ansible-inventory -i hosts.ini --list
nano setup.yml
Then paste the following content manually:
---
- name: Basic Server Setup
  hosts: local
  become: yes
  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes

    - name: Install curl
      apt:
        name: curl
        state: present
Press Ctrl + O to save.
Press Enter to confirm.
Press Ctrl + X to exit.

ansible-playbook -i hosts.ini setup.yml

curl --version

    
