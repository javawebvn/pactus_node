# pactus_node

# Auto Stake
##### Begin auto stake #####
apt install git curl wget vim -y && git config --global core.editor "vim" && git config --global core.fileMode false && rm -rf script_pactus && git clone https://github.com/toanbk/script_pactus.git && cd script_pactus && sed -i 's/filemode = true/filemode = false/' .git/config && chmod +x *.sh && touch .pass && echo '123123' > .pass

crontab -e

01 04 * * * /bin/bash -l -c '/root/script_pactus/staking.sh' > /var/log/pactus_staking.log 2>&1

cd script_pactus

sh balance.sh  # Check số dư

sh staking.sh # Auto Stake
###### Auto Stake #####





