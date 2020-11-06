---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504924"
---
# Get-AzureRmIotHub

## Áttekintés
Információt kap az előfizetésben szereplő IotHubs.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ListIotHubsByResourceGroup (alapértelmezett)
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetIotHubByName
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Információt kap az előfizetésben szereplő IotHubs.
Egy előfizetésben megtekintheti az összes IotHub-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott IotHub nevével.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmIotHub
```

Az előfizetésben lévő összes IotHubs kapja.

### 2. példa
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

Az előfizetéshez tartozó összes IotHubs megkapja az "myresourcegroup" nevű resourcegroup.

### 3. példa
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

Információt kap a "myiothub" nevű IotHub.

## PARAMÉTEREK

### -Name (név)
A IotHub neve

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A ResourceGroup neve

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
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

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Management. IotHub. models. PSIotHub
System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Command. Management. IotHub. models. PSIotHub, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null\]\]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

