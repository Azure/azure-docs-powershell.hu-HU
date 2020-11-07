---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: feba4e66483aba9e77817aa2b473d0d22ae7d882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679689"
---
# Get-AzureRmSiteRecoveryServer

## Áttekintés
Információt kap az aktuális boltozathoz regisztrált webhely-helyreállítási kiszolgálókról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSiteRecoveryServer** parancsmag a jelenlegi webhely-helyreállítási boltozathoz regisztrált Azure-webhelyek helyreállítási kiszolgálóiról tartalmaz információkat.

## Példák

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Típusú megjelenített
A kiszolgáló rövid nevét adja meg.

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A kiszolgáló nevét adja meg.

```yaml
Type: String
Parameter Sets: ByName
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

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRServer]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureRmSiteRecoveryServer](./Remove-AzureRmSiteRecoveryServer.md)
