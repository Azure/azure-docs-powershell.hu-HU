---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348269"
---
# Set-AzStorageFileContent

## SYNOPSIS
Feltölti egy fájl tartalmát.

## SZINTAXIS

### ShareName (alapértelmezett)
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Megosztás
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Címtár
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzStorageFileContent** parancsmag egy adott megosztáson található fájlba tölti fel a fájl tartalmát.

## PÉLDÁK

### 1. példa: Fájl feltöltése az aktuális mappába
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Ez a parancs egy DataFile37 nevű fájlt tölt fel az aktuális mappába CurrentDataFile néven a ContosoWorkingFolder mappában.

### 2. példa: Az aktuális mappa összes fájljának feltöltése
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

Ez a példa számos gyakori Windows PowerShell-parancsmagot és az aktuális parancsmagot használva tölti fel az aktuális mappában lévő összes fájlt a ContosoShare06 tároló gyökérmappába.
Az első parancs az aktuális mappa nevét kapja meg, és a $CurrentFolder tárolja.
A második parancs **a Get-AzStorageShare** parancsmagot használva szerezze be a ContosoShare06 nevű fájlmegosztást, majd tárolja azt a $Container változóban.
Az utolsó parancs az aktuális mappa tartalmát kapja meg, és a folyamat műveleti Where-Object átadja mindegyiket a Where-Object parancsmagnak.
Ez a parancsmag kiszűri azokat az objektumokat, amelyek nem fájlok, majd átadja a fájlokat a ForEach-Object parancsmagnak.
Ez a parancsmag minden fájlhoz futtat egy parancsfájlblokkot, amely létrehozza a megfelelő elérési utat, majd az aktuális parancsmag használatával tölti fel a fájlt.
Az eredménynek ugyanaz a neve és relatív pozíciója, mint az ebben a példában feltöltött többi fájl esetében.
A parancsfájlblokkokkal kapcsolatos további információkért írja be a `Get-Help about_Script_Blocks` .

### 3. példa: Töltsön fel egy helyi fájlt egy Azure-fájlba, és tartsa meg a helyi fájl SMB-tulajdonságait (Fájl-hozzárendelések, Fájl létrehozási ideje, Legutóbbi írási idő) az Azure-fájlban.
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

Ebben a példában egy helyi fájlt töltünk fel egy Azure-fájlba, és az Azure-fájl helyi SMB-tulajdonságait (Fájl-hozzárendelések, Fájlkészítési idő, Legutóbbi írási idő) is kiszolgaljuk.

## PARAMETERS

### -AsJob
Futtassa a parancsmagot a háttérben.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Ez a parancsmag feltölti a fájlt a paraméter által megadott mappába.
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

### -Force
Azt jelzi, hogy ez a parancsmag felülír egy meglévő Azure-tárfájlt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Azt jelzi, hogy ez a parancsmag a létrehozott vagy feltöltött **AzureStorageFile** objektumot adja vissza.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Egy fájl vagy mappa elérési útját adja meg.
Ez a parancsmag a tartalmat a paraméter által megadott fájlba vagy a paraméter által megadott mappában lévő fájlba tölti fel.
Ha mappát ad meg, ez a parancsmag a forrásfájl nevével azonos nevű fájlt hoz létre.
Ha olyan fájl elérési útját adja meg, amely nem létezik, ez a parancsmag létrehozza a fájlt, és annak a fájlba menti a tartalmat.
Ha megad egy már létező fájlt, és megadja a _Force_ paramétert, ez a parancsmag felülírja a fájl tartalmát.
Ha olyan fájlt ad meg, amely már létezik, és nem adja meg az Kényszerítve _értéket,_ ez a parancsmag nem módosítja a fájlt, és hibát ad vissza.
Ha olyan mappa elérési útját adja meg, amely nem létezik, ez a parancsmag nem módosítja, és hibát ad vissza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreserveSMBAttribute
A forrásfájl SMB-tulajdonságait (Fájl-hozzárendelések, Fájl létrehozási idő, Legutóbbi írási időpont) a célfájlban tartsa meg. Ez a paraméter csak Windows rendszeren érhető el.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Megosztás
Egy **CloudFileShare-objektumot** ad meg.
Ez a parancsmag feltölti a paraméter által megadott fájlba.
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
Ez a parancsmag feltölti a paraméter által megadott fájlba.

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

### -Source
A parancsmag által feltöltött forrásfájl.
Ha olyan fájlt ad meg, amely nem létezik, ez a parancsmag hibát ad vissza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzstorageDirectory](./Remove-AzStorageDirectory.md)

[New-AzstorageDirectory](./New-AzStorageDirectory.md)

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)
