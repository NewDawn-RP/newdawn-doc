---
sidebar_position: 2
title: Commandes Admin
---

# Liste des commandes admin


## Commandes de Give

### Se donner une arme / item

Cette commande vous permet de vous donner une arme ou un objet

```lua
/giveitem [ID] [Objet/Arme] [Quantité]
```

Les paramètres sont les suivants 

*ID* : ID du joueur voulu. Vous pouvez utiliser le mot-clé **me** au lieu de l'id lorsque vous souhaitez faire la commande sur vous-même

*Objet/Arme* : comme son nom l'indique on met ici le nom de l'objet ou de l'arme

*Quantité* : Tout simplement la quantité souhaité

#### Exemple d'utilisation

```lua
-- Pour se donner une M4
/giveitem me weapon_carbinerifle 1 

-- Pour donner un burger au joueur n°2
/giveitem 2 burger 4
```

## Commandes de Set

### Se mettre un job

Cette commande vous permet de vous donner une arme ou un objet

```lua
/setjob [ID] [NomDuJob] [NuméroGrade]
```

Les paramètres sont les suivants 

*ID* : ID du joueur voulu. Vous pouvez utiliser le mot-clé **me** au lieu de l'id lorsque vous souhaitez faire la commande sur vous-même

*NomDuJob* : Nom du job souhaité, par exemple *police* ou *taxi*

*NuméroGrade* : Tout simplement le numéro du grade souhaité, par exemple : 2 

#### Exemple d'utilisation

```lua
-- Pour se mettre le job police et le grade 1
/setjob me police 1 

-- Pour mettre le job taxi et le grade 1 au joueur n°2
/setjob 2 taxi 2
```


## Commandes Autres
