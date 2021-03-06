---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 55cee15e3b5327fa0a10def6e2090a77b68b207e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002421"
---
# New-AzStorageQueue

## SYNOPSIS
Tárterület-várólistát hoz létre.

## SZINTAXIS

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageQueue** parancsmag létrehoz egy tár várólistát az Azure-ban.

## PÉLDÁK

### 1. példa: Azure-tárterület várólistájának létrehozása
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

Ez a példa létrehoz egy queueabc nevű tárterület-várólistát.

### 2. példa: Több Azure storage queues létrehozása
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

Ez a példa több tárterület-várólistát hoz létre.
A .NET-karakterláncosztály Felosztás metódusát használja, majd átadja a neveket a folyamatnak.

## PARAMETERS

### -Környezet
Az Azure-tárterület környezetét határozza meg.
A parancsmagot a New-AzStorageContext hozhatja létre.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Megadja a várólistának a nevét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageQueue](./Get-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


