---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153707"
---
# Get-AzProviderOperation

## SYNOPSIS
Egy Azure-erőforrás-szolgáltató azure RBAC-n keresztül biztonságos műveleteit kapja meg.

## SZINTAXIS

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A Get-AzProviderOperation azure-erőforrás-szolgáltatók számára elérhetővé teszi a műveleteket.
A műveletek az Azure RBAC-ban egyéni szerepkörök létrehozásához is létrehozhatnak.
A parancs bemeneti karakterláncként (lehetséges helyettesítő karakter(ek)ekkel) határozza meg a megjelenítendő műveletek *részleteit. A Get-AzProviderOperation * használatával az összes Azure-erőforrás-szolgáltató összes műveletét lekérte. A Get-AzProviderOperation.Compute/* segítségével lekérte a Microsoft.Compute erőforrás-szolgáltató összes műveletét.

## PÉLDÁK

### 1. példa: Az összes művelet lekérte az összes szolgáltatót
```powershell
PS C:\> Get-AzProviderOperation *
```

### 2. példa: Adott erőforrás-szolgáltatóhoz szükséges műveletek lekérte
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### 3. példa: A virtuális gépeken elvégezhető összes művelet lekérte
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -OperationSearchString
A művelet keresési karakterlánca (lehetséges helyettesítő karakterekkel (*) karakterekkel)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés

## KAPCSOLÓDÓ HIVATKOZÁSOK
