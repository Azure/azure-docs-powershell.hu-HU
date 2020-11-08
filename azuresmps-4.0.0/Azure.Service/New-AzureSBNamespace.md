---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015988"
---
# New-AzureSBNamespace

## Áttekintés
Névteret hoz létre.

## SZINTAXISA

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **New-AzureSBNamespace** parancsmag létrehoz egy szolgáltatási névteret, amellyel az Azure rendszerhez használható a szolgáltatás busza.

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## Példák

### Példa 1: szolgáltatásbeli névtér létrehozása
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

A példákban létrehoz egy szolgáltatási névteret, amellyel az Azure-ban használható a szolgáltatás busza.
Mindkét példa tartalmazza a szükséges paramétereket, a paramétereket azonban csak az első tartalmazza.
A második példa akkor használható, ha mindkét paraméter pozícióval van megadva, és az értékek a szükséges sorrendben jelennek meg.

## PARAMÉTEREK

### -CreateACSNamespace
Azt adja meg, hogy a szolgáltatás névterén kívül létre kell-e hozni egy kapcsolódó ACS-névteret.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Az új névtér területét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Az új névtér nevét adja meg.

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

### -NamespaceType
Adja meg, hogy a névteret szeretné-e használni az üzenetküldési vagy az értesítési hubok számára.

```yaml
Type: NamespaceType
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureSBNamespace](./Remove-AzureSBNamespace.md)


