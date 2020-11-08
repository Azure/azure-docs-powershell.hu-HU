---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015670"
---
# Get-AzureApplicationGateway

## Áttekintés
Bekerül egy alkalmazás-átjáróba.

## SZINTAXISA

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureApplicationGateway** parancsmag meglévő Azure Application Gatewayt kap.

## Példák

### 1. példa: alkalmazás-átjáró beszerzése
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

Ez a parancs a ApplicationGateway06 nevű alkalmazás-átjárót kapja meg.

### 2. példa: az összes alkalmazás-átjáró beszerzése
```
PS C:\> Get-AzureApplicationGateway
```

Ez a parancs beilleszti az összes alkalmazás-átjárót az előfizetése alatt.

## PARAMÉTEREK

### -Name (név)
Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot kapja.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)

[Update-AzureApplicationGateway](./Update-AzureApplicationGateway.md)


