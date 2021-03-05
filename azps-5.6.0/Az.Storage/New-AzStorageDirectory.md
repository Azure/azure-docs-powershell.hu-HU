---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 6f44f1545eea4e515064873cdc77f8b34819fabc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002470"
---
# New-AzStorageDirectory

## SYNOPSIS
Címtárat hoz létre.

## SZINTAXIS

### ShareName (alapértelmezett)
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Megosztás
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Címtár
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageDirectory** parancsmag létrehoz egy címtárat.
Ez a parancsmag **egy CloudFileDirectory objektumot** ad vissza.

## PÉLDÁK

### 1. példa: Mappa létrehozása fájlmegosztásban
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

Ez a parancs létrehoz egy ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztásban.

### 2. példa: Mappa létrehozása egy fájlmegosztási objektumban megadott fájlmegosztásban
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

Ez a parancs **a Get-AzStorageShare** parancsmagot használva lekérte a ContosoShare06 nevű fájlmegosztást, majd a folyamat műveleti operátorával átadja az aktuális parancsmagnak.
Az aktuális parancsmag létrehozza a ContosoWorkingFolder nevű mappát a ContosoShare06-ban.

## PARAMETERS

### -ClientTimeoutPerRequest
Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.
Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.
Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Megadja a maximális párhuzamos hálózati hívásokat.
Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.
A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.
Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.
Az alapértelmezett érték 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
Egy Azure-tárterület környezetét adja meg.
Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
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

### -Directory
Mappát ad meg **CloudFileDirectory objektumként.**
Ez a parancsmag a paraméter által megadott helyen hozza létre a mappát.
Címtár beszerzéséhez használja a New-AzStorageDirectory parancsmagot.
Címtár beszerzéséhez használhatja Get-AzStorageFile parancsmagot is.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Path
A mappa elérési útját adja meg.
Ez a parancsmag létrehoz egy mappát a parancsmag által megadott elérési úthoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
A kérés kiszolgálói részében található időkorrekta hosszát adja meg.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Megosztás
Egy **CloudFileShare-objektumot** ad meg.
Ez a parancsmag létrehoz egy mappát a paraméter által megadott fájlmegosztásban.
**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.
Ez az objektum tartalmazza a tárterület környezetét.
Ha ezt a paramétert adja meg, ne adja meg a környezet *paramétert.*

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
A fájlmegosztás nevét adja meg.
Ez a parancsmag létrehoz egy mappát a paraméter által megadott fájlmegosztásban.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Get-AzstorageShare](./Get-AzStorageShare.md)

[New-AzstorageContext](./New-AzStorageContext.md)

[New-AzstorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzstorageDirectory](./Remove-AzStorageDirectory.md)
