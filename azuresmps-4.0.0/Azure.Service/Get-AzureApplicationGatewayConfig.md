---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015665"
---
# Get-AzureApplicationGatewayConfig

## Áttekintés
Az alkalmazás-átjáró konfigurációs környezetének beolvasása

## SZINTAXISA

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureApplicationGatewayConfig** parancsmag Azure Application Gateway-konfigurációs környezetet kap.
A kontextusban konfigurációs objektum és XML-konfiguráció is szerepel.
Az XML-konfigurációt mentheti fájlba.

## Példák

### 1. példa: alkalmazás-átjáró beállítása és mentése fájlba
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

Ez a parancs a ApplicationGateway06 nevű alkalmazás-átjáró konfigurációját kapja meg.
A parancs a megadott elérési útnak megfelelő fájlba menti a fájlt.

## PARAMÉTEREK

### -ExportToFile
Annak a fájlnak az elérési útját adja meg, amelyre a parancsmag XML formátumban menti a konfigurációt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag konfigurációs információkat kap.

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

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureApplicationGatewayConfig](./Set-AzureApplicationGatewayConfig.md)


