
# Créer un bot discord en python (introduction + démarrage)

## I - installation des prérequis
**Il faut impérativement que vous ayez appris les bases de python pour pouvoir utiliser cette librairie** 

si c'est le cas tappez sur votre **cmd**(invite de commandes) la **commande** suivante:

```
pip install discord.py
```
Si vous n'avez **pas de message d'erreur** c'est que vous avez **réussi** cette première partie
## II - création du bot discord 

donc là vous devez accéder au site de discord et crée un compte :https://discord.com/

puis dirigez-vous vers ce site : https://discord.com/developers/
là je vous conseille de regarder ma vidéo youtube pour mieux comprendre
là cliquez sur le boutton ```New Application```
donnez lui un nom et cliquez sur ```Create``` là vous créer une application pas un bot le bot est un utilisateur de discord comme toi et moi mais c'est une intelligence artificielle et tu le programmes tu peux lui ajouter une illustration si tu veux
maintenant dirrige toi vers l'onglet ```Bot et appuiesur le boutton ```Add Bot``` c'est une action irreversible mais tu peux toujours supprimer l'application si tu n'en veux plus du bot t'as une fenetre appuie sur ```Yes, do it!``` et voilà t'as ton utilisateur 
attend t'es parti sur discord pour voir si tu le trouves pas encore il faut l'inviter

## III - inviter le bot
dans l'onglet bot tu peux modifier sa photo de profile son nom d'utilisateur **ensuite tu as le token tu peux cliquer pour le reveler ou le copier mais attention il ne faut le donner à personne sinon on peut modifier ton bot si celà se produit click sur regenerate**
puuis il ya les permissions du bot moi je click sur administrator(administrateur) mais toi tu peux choisir voilà 
ensuite dirige toi vers l'onglet ```OAuth2``` dans scopes choisis bot il te donne un lien attends ne click pas va cocher la case adminostrator dans bot permissions
maintenant copier le lien et colle le dans une autre fenêtre là tu peux inviter ton bot dans les serveurs dans lesquels tubes administrateur je te conseille de créer un serveur d'essai parce que si le bot se met à supprimer des utilisateurs random ce serais la cata tu choisis tu continue il te fais un petit teste et voila ton bot est dans toon serveur!!!

## IV - premières lignes de code

si t'es allé voir tu as trouvé que ton bot est hors ligne c'est normal ou est python dans tout ça
mais ne t'en fait as c'est facile

tu peux taper ces lignes de code
normallement tu dois comprendre si t'as fait du python

```py
from discord.ext import commands

bot = commands.Bot(command_prefix="!")#là tu choisis le préfixe que tu veux moi j'ai choisi !
token = "<-- ici ton token celui dans l'onglet bot"
bot.run(token)
```
normalement le bot est en ligne mais on va ajouter quelques lignes pour savoir s'il est prêt
```py
from discord.ext import commands

bot = commands.Bot(command_prefix="!")#là tu choisis le préfixe que tu veux moi j'ai choisi !
token = "<-- ici ton token celui dans l'onglet bot"
@bot.event
async def on_ready():
    print("bot prêt")
bot.run(token)

```
la vous devez copier tout ça comme je l'ai mis ou vous aurez une erreur
j'explique c'est quoi async
async c'est pour dire que on_ready est unee fonction asyncrone
et @bot.event est un decorateur discord sais que c'est un evenement qui se declanche tout seul

# V - CONCLUSION
voilà vous savez comment allumer un bot discord c'est la fin on se voit la prochaine fois pour les premières commandes à plus
