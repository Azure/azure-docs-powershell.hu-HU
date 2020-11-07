---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: 05c5e797fa5ed56d6397b3881b368038a3d03a4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671390"
---
# Get-AzCognitiveServicesAccountType

## Áttekintés
Megkapja a rendelkezésre álló kognitív szolgáltatások számlatípust.

## SZINTAXISA

### GetAccountTypes (alapértelmezett)
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetAccountTypeWithName
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzCognitiveServicesAccountType** parancsmag a rendelkezésre álló kognitív Services típusú fiókokat az előfizetés alatt kapja meg.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

A rendelkezésre álló típusok listájának beszerzése

### 2. példa
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

A rendelkezésre álló típusok listájának beszerzése a westus.

### 3. példa
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

Ellenőrizze, hogy érvényes-e a név `Face` , a nevet a program visszaadja, ha az érvényes név.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A kognitív szolgáltatások fiók helye.

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeName
A kognitív szolgáltatások fiók típusa név.

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### System. string []

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
