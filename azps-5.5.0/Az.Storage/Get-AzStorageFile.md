---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164795"
---
# Get-AzStorageFile

## SYNOPSIS
Az elérési úthoz szükséges könyvtárakat és fájlokat sorolja fel.

## SZINTAXIS

### ShareName (alapértelmezett)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Megosztás
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Címtár
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzStorageFile** parancsmag felsorolja a megadott megosztás vagy címtár címtárát és fájljait.
Adja meg *a Path paramétert,* ha egy címtár vagy fájl adott elérési útba való példányát be kell szereznie.
Ez a parancsmag **az AzureStorageFile** és **az AzureStorageDirectory objektumokat adja** vissza.
Az **IsDirectory** tulajdonságot használva különböztetheti meg a mappákat és a fájlokat.

## PÉLDÁK

### 1. példa: A megosztásban található könyvtárak felsorolása
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

Ez a parancs csak a contososhare06-os megosztásban található könyvtárakat sorolja fel.
Először beolvassa a fájlokat és  a könyvtárakat, majd a pipeline operátorral átadja őket a where operátornak, majd elvet minden olyan objektumot, amelynek a típusa nem "AzureStorageFileDirectory".

### 2. példa: Fájlkönyvtárak felsorolása
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Ez a parancs felsorolja a ContosoWorkingFolder címtárban lévő fájlokat és mappákat a ContosoShare06 megosztás alatt.
Először a címtárpéldányt kapja meg, majd a **Get-AzStorageFile** parancsmagba befuttatva felsorolja a címtárat.

## PARAMETERS

### -ClientTimeoutPerRequest
Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.
Ha az előző hívás a megadott időszakon belül meghiúsul, ez a parancsmag újraüteme a kérelmet.
Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.

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
Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.
A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.
Ezzel a paraméterrel csökkenthetők a hálózati kapcsolattal kapcsolatos problémák alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.
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
Tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.

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
Ez a parancsmag a paraméter által megadott mappát kapja meg.
Címtár beszerzéséhez használja a New-AzStorageDirectory parancsmagot.
Könyvtár beszerzéséhez használhatja a **Get-AzStorageFile** parancsmagot is.

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
Ha nem adja meg a *Path* paramétert, a **Get-AzStorageFile** a megadott fájlmegosztásban vagy -címtárban lévő könyvtárakat és fájlokat sorolja fel.
Ha tartalmazza a *Path* paramétert, a **Get-AzStorageFile** egy címtár vagy fájl adott példányát adja vissza a megadott elérési útban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Egy kérés szolgáltatásoldali időkorlát-intervallumát adja meg másodpercben.
Ha a megadott időtartam eltelik, mielőtt a szolgáltatás feldolgozná a kérelmet, a Társzolgáltatás hibát ad vissza.

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
Ez a parancsmag a paraméter által megadott fájlmegosztásból kap egy fájlt vagy címtárat.
**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.
Ez az objektum a Tárterület környezett tartalmazza.
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
Ez a parancsmag a paraméter által megadott fájlmegosztásból kap egy fájlt vagy címtárat.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[New-AzstorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzstorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


