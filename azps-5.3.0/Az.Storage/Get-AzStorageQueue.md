---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479462"
---
# Get-AzStorageQueue

## SYNOPSIS
A tárterület-várólisták listája.

## SZINTAXIS

### QueueName (alapértelmezett)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzStorageQueue** parancsmag felsorolja az Azure Storage-fiókhoz társított társorokat.

## PÉLDÁK

### 1. példa: Az összes Azure Storage-várólisták felsorolása
```
PS C:\>Get-AzStorageQueue
```

Ez a parancs az aktuális tárfiók összes tár várólistájának listáját tartalmazza.

### 2. példa: Azure Storage-várólisták felsorolása helyettesítő karakterrel
```
PS C:\>Get-AzStorageQueue -Name queue*
```

Ez a parancs egy helyettesítő karaktert használva lekérte a várólistával kezdődik nevű tárolósorok listáját.

### 3. példa: Azure Storage-várólisták felsorolása a várólistán lévő név előtaggal
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

Ebben a példában az *Előtag* paramétert használva megjelenik a várólistával kezdődik nevű tárterület-várólisták listája.

## PARAMETERS

### -Környezet
Az Azure-tárterület környezetét határozza meg.
A **New-AzStorageContext** parancsmag használatával hozhatja létre.

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
Egy nevet ad meg.
Ha nincs megadva név, a parancsmag az összes várólistát felsorolja.
Ha teljes vagy részleges nevet ad meg, a parancsmag az összes olyan várólistát megkapja, amely megfelel a névmintának.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Előtag
Megadja a lekért várólisták nevében használt előtagot.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


