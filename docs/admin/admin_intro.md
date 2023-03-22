---
sidebar_position: 1
title: Introduction Admin
---

# Documentation Admin

Vous faites partie de l'équipe d'Administration de **New Dawn** et vous cherchez des infos pour vous sortir d'un bourbier immense ou simplement pour aider notre magnifique et ingénieux Responsable Dev' qu'est **Lexinor**, vous êtes tombé au bon endroit !

## Informations Générales

### Panel d'administration

Votre meilleur ami sur New Dawn sera le panel d'administration ou TxAdmin. En effet sur cette page vous pourrez y réaliser la plupart des actions d'administration, la seule contrainte sera votre grade. Rien de bien foufou mais voici quand même une liste des actions possible sur ce panel comme par exemple :
- Gérer la Whitelist
- Ban / Kick
- Mettre des notes sur les joueurs pour avoir un suivi les concernants
- Connaitre le nombre de joueurs présent
- Restart / Stop / Start le serveur
- Et d'autres choses..

### Contribuer à la documentation

Pour contribuer à la document vous pouvez utilser cet outil : [StackEdit](https://stackedit.io/app) pour la mie en page. Toutes vos modifications devront être envoyé sur le [Github de la doc](https://github.com/NewDawn-RP/newdawn-doc)

### Créer un item

Tout notre système d'inventaire utilise un script créé par l'équipe d'[Overextended](https://github.com/overextended). Le script en question est l'[Ox_Inventory](https://overextended.github.io/docs/ox_inventory), heuresement pour nous l'équipe d'**OX** a créé une belle documentation disponible ici : [Documentation](https://overextended.github.io/docs/)
Sur ce site vous pourrez y retrouver toutes les informations nécessaires concernants tous les scripts de cette équipe mais ici on se concentrera sur la partie qui concerne leur inventaire, [Ox_Inventory](https://overextended.github.io/docs/ox_inventory).

Pour vous simplifier le boulot, je vais vous résumer ici ce dont vous avez besoin pour nous aider à créer n'importe quel item que vous souhaitez, en sachant que vous ne pourrez pas forcément allez trop loin car une partie concerne exclusivement la partie Dev.

Pour créer un item c'est très simple. Il suffit de simplement définir plusieurs informations, voici un exemple ci-dessous :

```
['burger'] = {
    label = 'Burger',
    weight = 220,
    stack = true,
    close = true,
    client = {
        status = { hunger = 200000 },
        anim = { dict = 'mp_player_inteat@burger', clip = 'mp_player_int_eat_burger_fp' },
        prop = {
            model = 'prop_cs_burger_01',
            pos = { x = 0.02, y = 0.02, y = -0.02},
            rot = { x = 0.0, y = 0.0, y = 0.0}
        },
        usetime = 2500,
    }
}
```

Ne vous en faite pas je vais vous expliquer rapidement à quoi corresponds chaque partie, tout sera beaucoup plus clair après ça. 
Pour faire très simple voici une description de chaque informations que vous voyez au dessus.

- ['burger'] : *(Valeur Obligatoire)* Corresponds tout simplement au nom de l'item au niveau du système, vous utiliserez ce nom pour vous give cet item dans vos commandes. Par exemple : /giveitem me burger
- label : *(Valeur Obligatoire)* Corresponds à la valeur affichée dans l'inventaire. Vous pouvez choisir ce que vous voulez et elle peut être différente de la valeur du dessus. Ce ne sera que pour de l'affichage.
- weight : *(Valeur Obligatoire)* Le poids d'une unité de l'item. *Cette valeur est en grammes*
- stack : *(Valeur Obligatoire)* Est-ce que l'item est empilable. On la défini avec : **true** ou **false**
- degrade : *(Valeur Optionnelle)* Chiffre qui corresponds au nombre de minute avant que l'item se dégrade
- close : *(Valeur Optionnelle)* Tout simplement une valeur pour dire si on ferme l'inventaire lorsqu'on utilise l'item. On la défini avec : **true** ou **false**
- description : *(Valeur Optionnelle)* La description de l'objet
- consume : *(Valeur Optionnelle)* Combien d'item sera utilisé lors de l'utilisation de celui ci.
- allowArmed : *(Valeur Optionnelle)* Est-ce qu'on peut utiliser l'item en étant armé. On la défini avec : **true** ou **false**

#### Partie 'Client' d'un item

Dans l'item du dessus il y a une clé, "client". A cet endroit on y spécifiera toutes les choses à faire en parallèle de l'utilisation de l'item. Par exemple, dans le cas de notre burger nous faisons plusieurs actions à l'utilisation, je vous remet l'exemple du code ci-dessous :
```
client = {
        status = { hunger = 200000 },
        anim = { dict = 'mp_player_inteat@burger', clip = 'mp_player_int_eat_burger_fp' },
        prop = {
            model = 'prop_cs_burger_01',
            pos = { x = 0.02, y = 0.02, y = -0.02},
            rot = { x = 0.0, y = 0.0, y = 0.0}
        },
        usetime = 2500,
    }
```
Cet exemple de code va faire les choses suivantes :
- On va modifier la valeur "hunger" du joueur, c'est à dîre qu'on changera sa "faim". 
- Egalement on y voit d'autres informations comme la partie "anim" qui permet de choisir une animation particulière, en l'occurence on jouera une animation où le joueur mange quelque chose
- On va attacher un "prop" de burger sur la main du joueur pour ajouter du réalisme à l'animation
- Enfin on défini une durée d'animation pour le tout

### Mettre en ligne un item

Vous venez tout juste de créer un nouvel item et vous souhaitez le mettre sur le serveur. Il y a quelques pré-requis avant de faire ça :
1. Si votre item a besoin de faire des actions particulières il faut informer l'équipe de deveveloppement afin de voir avec elle le nécessaire à réaliser.
2. Rendez-vous sur ce site [Github](https://github.com/) et créez vous un compte, **si vous avez déjà un compte passez à la suite**.
3. Il vous faudra avoir l'accès à ce site : [Repository Ox_inventory version New Dawn](https://github.com/NewDawn-RP/ox_inventory). Si vous n'y avez pas accès arrêtez vous là et demander à **Lexinor** l'accès.
4. Une fois votre accès en poche, vous avez deux endroits où aller : 
    - [Ce lien, sera l'endroit où vous metterez le code de votre item](https://github.com/NewDawn-RP/ox_inventory/blob/main/data/items.lua)
    - [Ce lien pour y ajouter une potentielle miniature que vous voudriez ajouter](https://github.com/NewDawn-RP/ox_inventory/tree/main/web/images)
5. Pour ajouter une icône de miniature, rien de plus simple rendez-vous sur le lien ci-dessus et cliquez sur "Add files..". **Nommez vos miniature avec le même nom que l'item**. Par exemple votre item s'appelle ['cheese'] => votre image se nommera => cheese.png
6. Pour ajouter un item ça va un peu plus compliqué mais rien d'insurmontable. Voici les étapes à réaliser :
    - Encore une fois rendez-vous sur le lien donné plus haut puis cliquez sur l'icône en forme stylo. Vous entrerez en mode "edition" sur le fichier. 
    - Suite à ça, allez tout en bas du fichier. Juste avant la dernière accolade (**ceci est une accoalde => }**) collez simplement cette exemple d'item et changez les valeur que vous  avez besoin de changer.
        ['opium'] = {
            label = 'opium',
            weight = 500,
            stack = true,
            close = true,
            description = nil
        },
     - Respectez bien le format svp, si vous avez des questions et que vous n'êtes pas sûr de vous, n'hésitez pas à poser la question à un autre staff qui aurait la réponse, sinon demandez à Lexinor.
7. Pour terminer, il vous reste une dernière étape qui sera de "commit" (envoyez) vos modifications en mettant un petit message de titre pour expliquer ce que vous venez de faire ce qui nous aidera à tracer les ajouts fait sur le fichier :)
8. Confirmez en appuyant sur "Commit changes" et voilà, vous avez créé votre premier item !

**TRES IMPORTANT** Veuillez vérifier que vos nouveaux items et nouvelles icônes soient _*UNIQUE*_
