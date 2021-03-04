---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d4296acd16b29640fa8925d8482cca012be27b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940754"
---
# Get-AzStorageTable

## SYNOPSIS
A tárolótáblák listája.

## SZINTAXIS

### TableName (alapértelmezett)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzStorageTable** parancsmag felsorolja az Azure-beli tárfiókhoz társított tártáblákat.

## PÉLDÁK

### 1. példa: Az összes Azure Storage-tábla felsorolása
```
PS C:\>Get-AzStorageTable
```

Ez a parancs a Tárfiók összes tártábláját beveszi.

### 2. példa: Azure Storage-táblák felsorolása helyettesítő karakterrel
```
PS C:\>Get-AzStorageTable -Name table*
```

Ez a parancs egy helyettesítő karaktert használ a táblával kezdődik nevű tárolótáblák be szerezze be.

### 3. példa: Azure Storage-táblák felsorolása táblanév előtaggal
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Ez a parancs az *Előtag paraméter* segítségével beveszi a táblával kezdődik nevű tárolótáblákat.

## PARAMETERS

### -Környezet
A tárterület környezetét határozza meg.
A létrehozásához használhatja a New-AzStorageContext parancsmagot.

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
A tábla nevét adja meg.
Ha a tábla neve üres, a parancsmag felsorolja az összes táblát.
Ellenkező esetben felsorolja az összes olyan táblát, amely megfelel a megadott névnek vagy a normál név mintának.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Előtag
Megadja a lekért tábla vagy táblák nevében használt előtagot.
Ezzel a segítségével megkeresheti az összes olyan táblát, amely ugyanannak a karakterláncnak (például a táblának) az elején áll.

```yaml
Type: System.String
Parameter Sets: TablePrefix
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

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzstorageTable](./Remove-AzStorageTable.md)


