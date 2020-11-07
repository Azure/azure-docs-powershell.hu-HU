---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 48d37bf19ec6613ce1f42ee8cf7609bd6383e12f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842810"
---
# Get-AzAppServicePlan

## Áttekintés
Egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.

## SZINTAXISA

### S1
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzAppServicePlan** parancsmag egy Azure app-szolgáltatási csomagot kap a megadott erőforráscsoport számára.

## Példák

### 1. példa: alkalmazás-szolgáltatási terv beszerzése erőforráscsoporthoz
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

Ez a parancs beolvassa a ContosoASP nevű app-szolgáltatást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.

### 2. példa: a minden alkalmazás-szolgáltatási csomag beszerzése egy helyre
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

Ez a parancs a "Nyugat-amerikai" régióban található összes app-szolgáltatási csomagot beilleszti.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
Helyre 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Alkalmazás-szolgáltatási terv neve

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku

### Microsoft. Azure. Management. WebSites. models. ServerFarmCollection

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzAppServicePlan](./New-AzAppServicePlan.md)

[Remove-AzAppServicePlan](./Remove-AzAppServicePlan.md)

[Set-AzAppServicePlan](./Set-AzAppServicePlan.md)


