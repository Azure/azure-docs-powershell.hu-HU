---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145483"
---
# Get-AzRmStorageContainerImmutabilityPolicy

## SYNOPSIS
ImmutabilityPolicy of a Storage blob containers

## SZINTAXIS

### AccountName (alapértelmezett)
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountObject
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ContainerObject
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzRmStorageContainerImmutabilityPolicy parancsmag** ImmutabilityPolicy típusú blobtárolókat kap

## PÉLDÁK

### 1. példa: A Tárfiók nevét és tárolónevét tartalmazó Tár blobtároló ImmutabilityPolicy-ának lekérte
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

Ez a parancs immutabilityPolicy-t kap egy Tároló blobtárolóból, amely tárfióknevet és tárolónevet is ad.

### 2. példa: A Tárfiók objektummal és tárolónévvel egy Tárterület blobtároló ImmutabilityPolicy-ának lekérte
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

Ez a parancs immutabilityPolicy-t kap egy Tárfiók-objektummal és tárolónévvel.

### 3. példa: A Tártároló objektummal tárolt blobtároló ImmutabilityPolicy-ának lekérte
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

Ez a parancs immutabilityPolicy-t kap egy Tárolótároló objektumot tartalmazó Tár blobtárolóból.

## PARAMETERS

### -Container
Tárolóobjektum

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Tároló neve

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
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
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Etag
Immutability policy etag.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
Tárfiók objektum

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Tárfiók neve.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

### Microsoft.Azure.Commands.Management.Storage.Models.PSContainer

## KIMENETEK

### Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
