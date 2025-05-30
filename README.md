# website
currently just have a fastapi test in main.py
i run it using sudo uvicorn main:app --host 0.0.0.0 --port 80

I deployed to aws
security group rules for testing are to just have the ssh port and port 80 open to one ip I access from

I added a key for my desktop in the ui and generated a public key for it and put it in the authorized keys
ssh-keygen -y -f ~/.ssh/my-new-key.pem > my-new-key.pub
# on server
cat my-new-key.pub >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys

to setup i did
sudo apt install python3-fastapi
sudo apt install uvicorn