---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015480"
---
# Reset-AzureRoleInstance

## Áttekintés
Egyetlen szerepkör-példány vagy egy adott szerepkör minden szerepkör-példányának újraindítását vagy visszavonását kéri.

## SZINTAXISA

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **reset-AzureRoleInstance** parancsmag a bevezetésben futó szerepkör-példány újraindítását vagy átállítását kéri.
Ez a művelet szinkron módon fut.
Egy szerepkör-példány újraindításakor az Azure a példány offline állapotba kerül, újraindul a példány mögöttes operációs rendszer, és a példány visszakerül az internethez.
Minden olyan adatot, amely a helyi lemezre íródott, továbbra is elérhető lesz az újraindítások között.
A memóriában lévő összes adatot elvész.

A szerepkör-példányok újraképkezelése eltérő viselkedést eredményez a szerepkör típusától függően.
Ha a szerepkört áthelyezi a webhelyre vagy a munkatársi szerepkörre, az Azure a szerepkört offline állapotba helyezi, és az Azure Guest operációs rendszer új példányát írja a virtuális gépre.
A szerepkör ezután ismét online állapotba kerül.
VM-szerep esetén az Azure a szerepkör kapcsolat nélküli állapotba helyezése után újra alkalmazza a szerepkört az Ön által megadott egyéni képfájlra, és ismét online állapotba hozza a szerepkört.

Az Azure megkísérli a szerepkör átadásakor a helyi tárterület-erőforrásokban tárolt adatok megőrzését; átmeneti hardverhiba esetén azonban előfordulhat, hogy a helyi tárterület-erőforrás elveszhet.
Ha az alkalmazás az adatmegőrzést igényli, a tartós adatforrásba (például Azure-meghajtóra) való írás ajánlott.
Bármely olyan adat, amely a helyi tárterület-erőforrás által definiált eltérő helyi címtárba íródott, elvész, amikor a szerepkört átadta.

## Példák

### 1. példa: egy szerepkör-példány újraindítása
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

Ez a parancs újraindítja a MyWebRole_IN_0 nevű szerepkör-példányt a MySvc01 szolgáltatás bevezetési példányában.

### 2. példa: egy szerepkör-példány visszakeresése
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

Ez a parancs a MySvc01-Felhőbeli szolgáltatás bevezetési példányának szerepkör-példányait.

### 3. példa: a minden szerepkör-példány visszakeresése
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

Ez a parancs minden szerepkör-példányt átvesz a MySvc01 szolgáltatás üzembe helyezésére.

## PARAMÉTEREK

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Példánynév
Annak a szerepkör-példánynak a nevét adja meg, amelybe át szeretné majd indítani a feladatot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reboot
Azt adja meg, hogy a parancsmag újraindítja a megadott szerepkör-példányt, vagy ha nincs megadva, az összes szerepkör-példány.
Az *újraindítást* vagy a *Reimage* paramétert is tartalmaznia kell, de mindkettőt nem.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Reimage
Itt adhatja meg, hogy a parancsmag a megadott szerepkör-példányt, vagy ha nincs megadva, az összes szerepkör-példányt átadja-e.
Az *újraindítást* vagy a *Reimage* paramétert is tartalmaznia kell, de mindkettőt nem.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
A szolgáltatás nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A szerepkör példányait futtató központi telepítő környezetet adja meg.
Érvényes értékek: a termelés és a megállóhelyek.
A *DeploymentName* vagy a *slot* paramétert is használhatja, de mindkettőt nem.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRole](./Set-AzureRole.md)


