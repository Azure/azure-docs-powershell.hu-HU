---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492624"
---
# Get-AzureRmApiManagement

## Áttekintés
Listát vagy API-kezelési szolgáltatás leírását kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### All in előfizetés (alapértelmezett)
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Minden az erőforrás csoportban
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Adott API-kezelési szolgáltatás
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmApiManagement** parancsmag felsorolja az összes API-kezelési szolgáltatást az előfizetés vagy a megadott erőforráscsoport vagy egy bizonyos API-kezelés csoportban.

## Példák

### Példa 1: az API-kezelési szolgáltatások beszerzése
```
PS C:\>Get-AzureRmApiManagement
```

Ez a parancs az összes API-kezelési szolgáltatást beilleszti az előfizetésbe.

### 2. példa: az API-kezelési szolgáltatások beszerzése egy adott névvel
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

Ez a parancs a minden API-kezelési szolgáltatás bekerül a név mezőbe.

## PARAMÉTEREK

### -Name (név)
Az API-kezelési szolgáltatás nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amelyben a parancsmag az API-kezelési szolgáltatást kapja.

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
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

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ApiManagement. models. PsApiManagement]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzureRmApiManagement](./Backup-AzureRmApiManagement.md)

[Új – AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)

[Restore-AzureRmApiManagement](./Restore-AzureRmApiManagement.md)


