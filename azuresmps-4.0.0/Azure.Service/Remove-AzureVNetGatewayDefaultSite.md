---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015489"
---
# Remove-AzureVNetGatewayDefaultSite

## Áttekintés
Eltávolítja az alapértelmezett útvonalat a kényszerített bújtatási forgalomhoz.

## SZINTAXISA

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureVNetGatewayDefaultSite** parancsmag eltávolítja az alapértelmezett útvonalat a helyszíni webhelyre a kényszerített bújtatási forgalomhoz.
Ez a parancsmag eltávolítja egy virtuális hálózat Azure virtuális magánhálózati (VPN) átjárójának útvonalát.

## Példák

### 1. példa: az útvonal eltávolítása az alapértelmezett webhelyre
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

Ez a parancs eltávolítja az alapértelmezett webhelynek az ContosoVNet01 nevű virtuális hálózat virtuális magánhálózaton található útvonalát.

## PARAMÉTEREK

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
Virtuális hálózatot ad meg.
Ez a parancsmag eltávolítja a virtuális hálózat VPN-átjárójának alapértelmezett útvonalát, amelyet ez a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Set-AzureVNetGatewayDefaultSite](./Set-AzureVNetGatewayDefaultSite.md)
