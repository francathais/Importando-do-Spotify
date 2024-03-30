import spotipy
from spotipy.oauth2 import SpotifyClientCredentials

# Insira suas credenciais do cliente aqui
client_id = 'c6fb5f43c096450182ab7d5b396ac59d'
client_secret = '9a2f578cd9574279b6aada0c34ab3ce6'

# Configurar autenticação
client_credentials_manager = SpotifyClientCredentials(client_id=client_id, client_secret=client_secret)
sp = spotipy.Spotify(client_credentials_manager=client_credentials_manager)

# Link do podcast "Mundo Freak Confidencial" no Spotify
podcast_uri = 'https://open.spotify.com/show/7nysE4xNmZZ36ru0FrNGLg'  # Substitua pelo link do seu podcast

# Obter informações do podcast
podcast_info = sp.show(podcast_uri)

# Imprimir nome e datas dos episódios
print("Nome do Podcast: ", podcast_info['name'])

episodes = podcast_info.get('episodes', {}).get('items', [])
if not episodes:
    print("Nenhum episódio encontrado para este podcast.")
else:
    print("Episódios:")
    for episode in episodes:
        print("Nome: ", episode['name'])
        print("Data de lançamento: ", episode['release_date'])
        print()
