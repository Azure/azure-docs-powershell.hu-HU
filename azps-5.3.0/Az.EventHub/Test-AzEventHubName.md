---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469818"
---
# Test-AzEventHubName

## SYNOPSIS
A megadott Névtérnév vagy Alias elérhetőségének ellenőrzése (DR konfiguráció neve)

## SZINTAXIS

### NamespaceCheckNameAvailabilitySet (alapértelmezett)
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasCheckNameAvailabilitySet
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Test-AzEventhubName parancsmag** ellenőrzi, hogy rendelkezésre áll-e a NameSpace név vagy alias (DR configuration name)

## PÉLDÁK

### 1. példa
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

A "MyNameSapceName" név elérhetőségének állapotát adja vissza Igaz értékként, ha elérhető.

### 2. példa
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

A "MyNameSapceName" név "MyNameSapceName" elérhetőségének állapotát adja vissza hamisként, ok nélkül.

### 3. példa
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

A "MyNameSapceName" névtér "MyNameSapceName" aliasának elérhetőségi állapotát adja vissza Igaz értékként, ha elérhető.

## PARAMETERS

### -AliasName
DR Configuration Name - Alias Name

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Namespace
Eventhub Namespace Name

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
