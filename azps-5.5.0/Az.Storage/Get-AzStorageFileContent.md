---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143890"
---
# Get-AzStorageFileContent

## SYNOPSIS
Letölti egy fájl tartalmát.

## SZINTAXIS

### ShareName (alapértelmezett)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Megosztás
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Címtár
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Fájl
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzStorageFileContent** parancsmag letölti egy fájl tartalmát, majd egy Ön által megadott célhelyre menti.
Ez a parancsmag nem adja vissza a fájl tartalmát.

## PÉLDÁK

### 1. példa: Fájl letöltése egy mappából
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Ez a parancs letölt egy CurrentDataFile nevű fájlt a ContosoWorkingFolder mappából a ContosoShare06 fájlmegosztásból az aktuális mappába.

### 2. példa: A mintafájlmegosztás alatti fájlok letöltése
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

Ez a példa letölti a mintafájlmegosztás alatti fájlokat

### 3. példa: Töltsön le egy Azure-fájlt egy helyi fájlba, és a helyi fájlban tartsa meg az Azure-fájl SMB tulajdonságait (fájl-hozzárendelések, fájl létrehozási ideje, legutóbbi írási idő).
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

Ez a példa letölt egy Azure-fájlt egy helyi fájlba, és a helyi fájlban az Azure-fájl SMB-tulajdonságait (Fájl-hozzárendelések, Fájlkészítési idő, Fájl legutóbbi írási ideje) is használja.

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

### -CheckMd5
Azt adja meg, hogy ellenőrizze-e a letöltött fájl Md5-ös összegét.

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
Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben. Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet. Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.

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
Megadja a maximális párhuzamos hálózati hívásokat. Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával. A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal. Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben. Az alapértelmezett érték 10.

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
Az Azure Storage környezetét adja meg. Környezet lekérte a New-AzStorageContext parancsmagot.

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

### -Destination
Megadja a cél elérési útját.
Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott helyre.
Ha olyan fájl elérési útját adja meg, amely nem létezik, ez a parancsmag hozza létre a fájlt, és a tartalmat az új fájlba menti.
Ha megad egy már létező fájl elérési útját, és megadja a *Force* paramétert, a parancsmag felülírja a fájlt.
Ha megadja egy meglévő fájl elérési útját, és nem adja meg az Kényszerítés *parancsot,* a parancsmag a továbblépés előtt megkérdezi.
Ha megadja egy mappa elérési útját, ez a parancsmag megkísérli létrehozni az Azure-tárfájl nevét tartalmazó fájlt.

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

### -Directory
Mappát ad meg **CloudFileDirectory objektumként.**
Ez a parancsmag a paraméter által megadott mappában lévő fájl tartalmát kapja meg.
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

### -File
Egy fájlt ad meg **CloudFile-objektumként.**
Ez a parancsmag a paraméter által megadott fájlt kapja meg.
**CloudFile-objektum** beszerzéséhez használja a Get-AzStorageFile parancsmagot.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
Ha olyan fájl elérési útját adja meg, amely nem létezik, ez a parancsmag hozza létre a fájlt, és a tartalmat az új fájlba menti.
Ha megad egy már létező fájl elérési útját, és megadja a *Force* paramétert, a parancsmag felülírja a fájlt.
Ha megadja egy meglévő fájl elérési útját, és nem adja meg az Kényszerítés *parancsot,* a parancsmag a továbblépés előtt megkérdezi.
Ha megadja egy mappa elérési útját, ez a parancsmag megkísérli létrehozni az Azure-tárfájl nevét tartalmazó fájlt.

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
Azt jelzi, hogy ez a parancsmag a letöltött **AzureStorageFile** objektumot adja vissza.

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
A fájl elérési útját adja meg.
Ez a parancsmag a paraméter által megadott fájl tartalmát kapja meg.
Ha a fájl nem létezik, ez a parancsmag hibát ad vissza.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
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
A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez. Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.

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
Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott megosztásban.
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
Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott megosztásban.

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

### Microsoft.Azure.Storage.File.CloudFile

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


