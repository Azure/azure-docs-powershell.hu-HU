---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016527"
---
# Get-AzureVNetSite

## Áttekintés
A List objektum lekérdezése az Azure virtuális hálózatokkal kapcsolatos információkat tartalmazza.

## SZINTAXISA

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureVNetSite** parancsmag olyan lista-objektumot kap, amely az aktuális előfizetéshez tartozó Azure virtuális hálózatokra vonatkozó információkat tartalmaz.
Ha megad egy virtuális hálózat nevét, akkor csak az adott virtuális hálózatra vonatkozó információk jelennek meg.

## Példák

### 1. példa: információk kérése az aktuális előfizetéshez tartozó összes virtuális hálózatról
```
PS C:\> Get-AzureVNetSite
```

Ez a parancs a jelenlegi előfizetésben lévő összes virtuális hálózatról információt kap.

### 2. példa: információk kérése egy adott virtuális hálózatról az aktuális előfizetésben
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

Ez a parancs csak a MyProductionNetwork virtuális hálózatra keres információkat.

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

### -VNetName
Megadja a virtuális hálózati nevet, amellyel információt ad vissza.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureVNetConfig](./Get-AzureVNetConfig.md)

[Remove-AzureVNetConfig](./Remove-AzureVNetConfig.md)

[Set-AzureVNetConfig](./Set-AzureVNetConfig.md)


