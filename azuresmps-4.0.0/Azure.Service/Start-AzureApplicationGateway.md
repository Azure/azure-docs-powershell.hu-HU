---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015779"
---
# Start-AzureApplicationGateway

## Áttekintés
Elindítja az alkalmazás-átjárót.

## SZINTAXISA

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureApplicationGateway** parancsmag egy alkalmazás-átjárót indít el.

## Példák

### 1. példa: alkalmazás-átjáró indítása
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

Ez a parancs elindítja a ApplicationGateway06 nevű alkalmazás-átjárót.

## PARAMÉTEREK

### -Name (név)
Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag elindul.

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

### Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[Új – AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)

[Update-AzureApplicationGateway](./Update-AzureApplicationGateway.md)


