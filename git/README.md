git config --global user.name "Charles Fourdrignier"
git config --global user.email charles.fourdrignier@gmail.com

ssh-keygen -t rsa -b 4096 -C "charles.fourdrignier@gmail.com"

eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
