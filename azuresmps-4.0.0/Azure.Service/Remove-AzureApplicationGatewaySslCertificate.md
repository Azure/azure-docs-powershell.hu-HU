---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016494"
---
# Remove-AzureApplicationGatewaySslCertificate

## Áttekintés
Egy alkalmazás-átjárótól származó SSL-tanúsítvány eltávolítása.

## SZINTAXISA

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureApplicationGatewaySslCertificate** parancsmag az alkalmazás-átjárók SSL-tanúsítványát távolítja el.

## Példák

### 1. példa: SSL-tanúsítvány eltávolítása
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

Ez a parancs eltávolítja a SslCertificate13 nevű SSL-tanúsítványt a ApplicationGateway08 nevű alkalmazás-átjáróból.

## PARAMÉTEREK

### -CertificateName
Az SSL-tanúsítvány nevét adja meg.
Ez a parancsmag eltávolítja a paraméter által megadott tanúsítványt.

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

### -Name (név)
Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag eltávolítja az SSL-tanúsítványt.

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

### Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureApplicationGatewaySslCertificate](./Add-AzureApplicationGatewaySslCertificate.md)

[Get-AzureApplicationGatewaySslCertificate](./Get-AzureApplicationGatewaySslCertificate.md)
