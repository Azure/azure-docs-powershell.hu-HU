---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672224"
---
# Get-AzureRmDataLakeAnalyticsAccount

## Áttekintés
Információt kap az adattó Analytics-fiókjáról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### All in előfizetés (alapértelmezett)
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Minden az erőforrás csoportban
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Konkrét fiók
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataLakeAnalyticsAccount** parancsmag információkat kap az Azure-alapú adattó Analytics-fiókjáról.

## Példák

### 1. példa: adatok beolvasása az adattó Analytics-fiókjával
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.

## PARAMÉTEREK

### -Name (név)
Az adattó-Analytics-fiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSDataLakeAnalyticsAccount
A megadott fiók adatai.

### Lista<PSDataLakeAnalyticsAccount>
A megadott erőforráscsoport vagy-előfizetés fiókjainak listája.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmDataLakeAnalyticsAccount](./New-AzureRmDataLakeAnalyticsAccount.md)

[Remove-AzureRmDataLakeAnalyticsAccount](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[Set-AzureRmDataLakeAnalyticsAccount](./Set-AzureRmDataLakeAnalyticsAccount.md)

[Teszt-AzureRmDataLakeAnalyticsAccount](./Test-AzureRmDataLakeAnalyticsAccount.md)


