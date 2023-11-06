---
sidebar_position: 3
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

-- Pour donner 4 burgers au joueur n°2
/giveitem 2 burger 4
```

## Commandes de Set

### S'attribuer un job

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

### S'attribuer une faction

Cette commande vous permet de vous donner une arme ou un objet

```lua
/setfaction [ID] [NomDeLaFaction] [NuméroGrade]
```

Les paramètres sont les suivants 

*ID* : ID du joueur voulu. Vous pouvez utiliser le mot-clé **me** au lieu de l'id lorsque vous souhaitez faire la commande sur vous-même

*NomDeLaFaction* : Nom de la faction souhaitée, par exemple *mafia* ou *cartel*

*NuméroGrade* : Tout simplement le numéro du grade souhaité, par exemple : 2 

#### Exemple d'utilisation

```lua
-- Pour se mettre la faction cartel et le grade 1
/setfaction me cartel 1 

-- Pour mettre la faction mafia et le grade 1 au joueur n°2
/setfaction 2 mafia 2
```

## Commandes Autres
