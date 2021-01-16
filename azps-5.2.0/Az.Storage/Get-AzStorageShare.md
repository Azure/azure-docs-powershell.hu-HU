---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: b6323cd751d25038ff6705cee45594796d782326
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349578"
---
# Get-AzStorageShare

## SYNOPSIS
Lekérte a fájlmegosztások listáját.

## SZINTAXIS

### MatchingPrefix (alapértelmezett)
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Specific
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzStorageShare** parancsmag lekérte egy tárfiók fájlmegosztási listáját.

## PÉLDÁK

### 1. példa: Fájlmegosztás létrehozása
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

Ez a parancs a ContosoShare06 nevű fájlmegosztást kapja meg.

### 2. példa: Az összes olyan fájlmegosztás lekérte, amely karakterláncmal kezdődik
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

Ez a parancs a Contoso névvel kezdődik fájlmegosztásokat is beveszi.

### 3. példa: Az összes fájlmegosztás lekérte egy adott környezetben
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

Az első parancs a **New-AzStorageContext** parancsmagot használva hoz létre környezetet a *Helyi* paraméter használatával, majd ezt a környezetobjektumot a $Context változóban tárolja.
A második parancs a helyi menüben tárolt környezetobjektum fájlmegosztási $Context.

### 4. példa: Fájlmegosztási pillanatfelvétel adott megosztási névvel és SnapshotTime-val
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

Ez a parancs egy fájlmegosztási pillanatképet kap adott megosztási névvel és SnapshotTime-val.

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
Az Azure Storage környezetét adja meg.
Környezet beszerzéséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.

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
A fájlmegosztás nevét adja meg.
Ez a parancsmag a paraméter által megadott fájlmegosztást kapja meg, vagy semmit sem, ha olyan fájlmegosztás nevét adja meg, amely nem létezik.

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Előtag
A fájlmegosztások előtagját határozza meg.
Ez a parancsmag olyan fájlmegosztásokat kap, amelyek megegyeznek a paraméter által megadott előtaggal, vagy nem kap fájlmegosztásokat, ha egyetlen fájlmegosztás sem felel meg a megadott előtagnak.

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
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

### -SnapshotTime
SnapshotTime of the file share snapshot to be received.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzstorageShare](./New-AzStorageShare.md)

[Remove-AzstorageShare](./Remove-AzStorageShare.md)
