---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836301"
---
# Get-AzDataLakeStoreItemPermission

## Áttekintés
Az adattó-tárolóban lévő fájl vagy mappa engedélyét adja meg.

## SZINTAXISA

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDataLakeStoreItemPermission** parancsmag az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét kapja.

## Példák

### 1. példa: a fájlhoz tartozó engedélyek beállítása
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

Ez a parancs beilleszti a fájlhoz tartozó engedély oktálisát.

## PARAMÉTEREK

### -Fiók
Az adattó áruházbeli fiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Path (elérési út)
A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance

## KIMENETEK

### System. String

## MEGJEGYZI
* Alias: Get-AdlStoreItemPermission

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzDataLakeStoreItemPermission](./Set-AzDataLakeStoreItemPermission.md)


