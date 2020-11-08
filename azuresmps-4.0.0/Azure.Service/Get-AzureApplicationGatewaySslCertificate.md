---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015664"
---
# Get-AzureApplicationGatewaySslCertificate

## Áttekintés
Az alkalmazás-átjáró tanúsítványait kapja.

## SZINTAXISA

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureApplicationGatewaySslCertificate** parancsmag Secure Sockets Layer (SSL) tanúsítványokat kap az Azure Application Gateway rendszerhez.

## Példák

### Példa 1: SSL-tanúsítvány beszerzése
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

Ez a parancs egy SslCertificate13 nevű SSL-tanúsítványt kap a ApplicationGateway08 nevű alkalmazás-átjáróban.

### 2. példa: az összes SSL-tanúsítvány beszerzése
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

Ez a parancs a ApplicationGateway08 nevű alkalmazás-átjáró összes SSL-tanúsítványát lekapja.

## PARAMÉTEREK

### -CertificateName
Az SSL-tanúsítvány nevét adja meg.
Ez a parancsmag a paraméter által megadott tanúsítványt kapja meg.

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
Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag az SSL-tanúsítványt kapja.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, List<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureApplicationGatewaySslCertificate](./Add-AzureApplicationGatewaySslCertificate.md)

[Remove-AzureApplicationGatewaySslCertificate](./Remove-AzureApplicationGatewaySslCertificate.md)
