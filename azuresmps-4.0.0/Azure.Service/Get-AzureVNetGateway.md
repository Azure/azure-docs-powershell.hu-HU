---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016279"
---
# Get-AzureVNetGateway

## Áttekintés
Virtuális hálózati átjáró állapotát kapja meg.

## SZINTAXISA

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureVNetGateway** parancsmag egy meglévő virtuális hálózati átjáró állapotát kapja meg.

## Példák

### Példa 1: virtuális hálózati átjáró állapotának beszerzése
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

Ez a parancs azt kapja meg, hogy a virtuális hálózat átjárója a ContosoVN07 nevű virtuális hálózat átjárójának állapotát adja meg.

## PARAMÉTEREK

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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
A virtuális hálózati átjárót tartalmazó virtuális hálózat, amelynek a parancsmagja megkapja az állapotát.

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

[Új – AzureVNetGateway](./New-AzureVNetGateway.md)

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Átméretezés-AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


