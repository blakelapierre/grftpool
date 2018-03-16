FROM blakelapierre/grft

EXPOSE 8070
VOLUME daemon-data
VOLUME wallet-data

CMD cd coin/bin && if [ ! -f /wallet-data/container ]; then ./graft-wallet-rpc --data-dir /wallet-data -g -w /wallet-data/container; fi; ./graft-wallet-rpc --daemon-address daemon --daemon-port 8888 --rpc-bind-port 7777 --rpc-bind-port 7777 --data-dir /wallet-data -w /wallet-data/container