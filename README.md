# Guide d'utilisation du Projet

Ce projet a été testé sur un sous-système Ubuntu via Windows Subsystem for Linux (WSL).

## Utilisation de WSL

Pour utiliser WSL, suivez ces étapes :

1. Mettez à jour WSL :
    ```bash
    wsl --update
    ```

2. Installez Ubuntu :
    ```bash
    wsl --install -d Ubuntu
    ```

## Utilisation sur Google Colab

Google Colab ne permettant pas d'exécuter des modèles d'IA aussi lourds localement, j'ai dû utiliser un environnement local.

Si vous rencontrez des difficultés à exécuter un modèle d'IA sur Google Colab, suivez ces étapes sur la machine Ubuntu :

1. Mettez à jour les paquets :
    ```bash
    sudo apt update
    ```

2. Installez Jupyter Notebook :
    ```bash
    pip install notebook
    ```

3. Installez Jupyter Core :
    ```bash
    sudo apt install jupyter-core
    ```

4. Installez Jupyter HTTP Over WebSocket :
    ```bash
    pip install jupyter_http_over_ws
    ```

5. Activez l'extension du serveur Jupyter :
    ```bash
    jupyter server extension enable --py jupyter_http_over_ws
    ```

6. Lancez le notebook :
    ```bash
    python3 -m notebook
    ```

Si la commande `jupyter server extension enable --py jupyter_http_over_ws` ne fonctionne pas, vous pouvez utiliser la commande suivante pour exécuter le serveur.

Une fois le notebook lancé, recherchez dans le terminal le lien à utiliser. Il aura la forme suivante : `http://localhost:8888/tree?token={token}`.

Sur Google Colab, sur la machine hôte, recherchez la possibilité de vous connecter à un environnement d'exécution local en cliquant sur la liste déroulante en haut à droite. Renseignez le lien obtenu dans votre terminal et exécutez le projet.

