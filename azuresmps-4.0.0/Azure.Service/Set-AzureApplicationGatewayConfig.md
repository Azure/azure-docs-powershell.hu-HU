---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016429"
---
# Set-AzureApplicationGatewayConfig

## Áttekintés
Az alkalmazás-átjáró beállítása.

## SZINTAXISA

### Engedélybeállítások
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureApplicationGatewayConfig** parancsmag egy alkalmazás-átjárót konfigurál.

## Példák

### 1. példa: az alkalmazás-átjáró konfigurálása konfigurációs objektum használatával
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

Az első parancs a **Get-AzureApplicationGatewayConfig** parancsmag használatával kapja meg a ApplicationGateway02 nevű alkalmazás-átjáró konfigurációs objektumát.
A parancs a $ConfigReturnObject változóban tárolja.

A második parancs beállítja a ApplicationGateway06 nevű alkalmazás konfigurációját az $ConfigReturnObject változóban tárolt Application Gateway Configuration objektum használatával.

### 2. példa: az alkalmazás-átjáró konfigurálása konfigurációs fájllal
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

Ez a parancs beállítja a ApplicationGateway06 nevű alkalmazás konfigurációját a megadott helyen, az Application Gateway konfigurációs fájljával.

### 3. példa: konfiguráció módosítása konfigurációs objektum használatával
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

Az első parancs a **Get-AzureApplicationGatewayConfig** parancsmag használatával kapja meg a ApplicationGateway06 nevű alkalmazás-átjáró konfigurációs objektumát.
A parancs a $ConfigReturnObject változóban tárolja.

A második parancs a $ConfigReturnObjectban tárolt objektum egy **port** tulajdonságához rendeli a portszámot.

A végleges parancs átadja a frissített $ConfigReturnObject az aktuális parancsmagnak.

## PARAMÉTEREK

### -Config
Az Application Gateway konfigurációs objektumát adja meg.
Ez a parancsmag azt a konfigurációt rendeli hozzá, amelyet ez a paraméter egy alkalmazás-átjáróhoz ad meg.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Engedélybeállítások
A konfigurációs fájl elérési útját adja meg XML-formátumban az alkalmazás-átjárók számára.
Ez a parancsmag azt a konfigurációt rendeli hozzá, amelyet ez a paraméter egy alkalmazás-átjáróhoz ad meg.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag konfigurálva van.

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

### System. string, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## KIMENETEK

### Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


