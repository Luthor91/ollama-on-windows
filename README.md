Ce projet à été testé sur un sous système Ubuntu sur Windows grâce à WSL.

Pour utiliser WSL : 
Renseignez ces commandes sur un terminal : 
wsl --update
wsl --install -d Ubuntu

Google Collab ne permettant pas de faire tourner quelque chose d'aussi lourd qu'un modèle d'IA, j'ai dû utiliser un environnement local.
Si vous avez du mal à faire tourner un modèle d'IA sur Collab, sur la machine Ubuntu j'ai rentré ces commandes : 

sudo apt update
pip install notebook
sudo apt install jupyter-core
pip install jupyter_http_over_ws
jupyter server extension enable --py jupyter_http_over_ws
python3 -m notebook  

A noter que si la commande "jupyter server extension enable --py jupyter_http_over_ws" ne fonctionne pas, la commande suivante permet d'exécuter le serveur.

Cherchez dans le terminal un lien à utiliser, de mon côté c'est un lien sous la forme  http://localhost:8888/tree?token={token}

Sur Google Collab sur la amchine hôte, cherchez à vous connecter à un environnement d'exécution local, en cliquant sur la liste déroulante en haut à droite.
Renseignez le lien qui était dans votre terminal.
Executez le projet.
