---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015736"
---
# Add-AzureApplicationGatewaySslCertificate

## Áttekintés
SSL-tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.

## SZINTAXISA

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureApplicationGatewaySslCertificate** parancsmag egy biztonságos szoftvercsatorna-RÉTEGET (SSL-tanúsítványt) ad az Azure Application Gateway-nek.

## Példák

### 1. példa: SSL-tanúsítvány felvétele
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

Ez a parancs hozzáadja a SslCertificate13 nevű SSL-tanúsítványt a ApplicationGateway08 nevű alkalmazási átjáróhoz.
A parancs a tanúsítványfájl elérési útját és a tanúsítvány jelszavát adja meg.

## PARAMÉTEREK

### -CertificateFile
Az SSL-tanúsítványfájl elérési útját adja meg.
Ez a parancsmag hozzáadja a tanúsítványt a fájlban, amelyet a paraméter határoz meg.

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

### -CertificateName
Az SSL-tanúsítvány nevét adja meg.
Ez a parancsmag hozzáadja a paramétert megadó tanúsítványt.

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
Annak az alkalmazásnak az átjárójának a neve, amelyhez a parancsmag hozzáadja az SSL-tanúsítványt.

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

### -Jelszó
Annak az SSL-tanúsítványnak a jelszava, amelyet a parancsmag ad.

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

[Get-AzureApplicationGatewaySslCertificate](./Get-AzureApplicationGatewaySslCertificate.md)

[Remove-AzureApplicationGatewaySslCertificate](./Remove-AzureApplicationGatewaySslCertificate.md)
