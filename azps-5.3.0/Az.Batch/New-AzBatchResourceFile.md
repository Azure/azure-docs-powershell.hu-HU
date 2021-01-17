---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478258"
---
# New-AzBatchResourceFile

## SYNOPSIS
Létrehozza az erőforrásfájlt `New-AzBatchTask` használatra.

## SZINTAXIS

### HttpUrl (alapértelmezett)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Létrehozza az erőforrásfájlt `New-AzBatchTask` használatra.

## PÉLDÁK

### 1. példa: Erőforrásfájl létrehozása egyetlen fájlra mutató HTTP URL-címből
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`HTTP-url-címre hivatkozó url-címet hoz létre.

### 2. példa: Erőforrásfájl létrehozása Egy Azure Storage tároló URL-címében
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Létrehoz `PSResourceFile` egy, az Azure Storage tároló URL-címére hivatkozó címet. A rendszer a tárolóban lévő összes fájlt letölti a megadott mappába.

### 3. példa: Erőforrásfájl létrehozása automatikus tárolónévből
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Létrehoz `PSResourceFile` egy, az Automatikus tároló tároló nevére hivatkozó nevet. A rendszer a tárolóban lévő összes fájlt letölti a megadott mappába.

## PARAMETERS

### -AutoStorageContainerName
A tároló neve az automatikus tárfiókban.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
A blobelőtagot használja, amikor blobokat tölt le egy Azure Storage-tárolóból.
Csak azok a blobok tölthetők le, amelyeknek a neve a megadott előtaggal kezdődik.
Ez az előtag lehet egy részleges fájlnév vagy egy alkönyvtár.
Ha nincs megadva előtag, a rendszer a tárolóban lévő összes fájlt letölti.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -FileMode
A fájlengedélyek módjának attribútumát oktális formátumban kapja meg.
Ez a tulajdonság csak akkor érvényes, ha az erőforrásfájl egy Linux-csomópontra van letöltve.
Ha ez a tulajdonság nincs megadva linuxos csomóponthoz, akkor az alapértelmezett érték 0770.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
A számítási csomópontnak az a helye, amelyre le szeretné tölteni a fájlt(a) a feladat munkakönyvtárához képest. Ha a HttpUrl paraméter meg van adva, a FilePath paraméter megadása kötelező, és bemutatja a fájl letöltési elérési útját, a fájlnévvel együtt. Ellenkező esetben, ha az AutoStorageContainerName vagy a StorageContainerUrl paraméter meg van adva, a FilePath megadása nem kötelező, és az a könyvtár, amelybe le kell töltenie a fájlokat. Abban az esetben, ha a FilePath címtárként van használva, a bemeneti adatokhoz társított esetleges címtárszerkezetek teljes egészében megmaradnak, és a megadott FilePath-címtárhoz lesznek hozzáfűzve. A megadott relatív útvonal nem tud kijönni a tevékenység munkakönyvtárból (például a ".." használatával).

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
A letölteni kívánt fájl URL-címe.
Ha az URL-cím Azure Blob Storage, névtelen hozzáféréssel is olvashatónak kell lennie; azaz a Batch szolgáltatás nem ad meg hitelesítő adatokat a blob letöltésekor.
Kétféleképpen lehet ilyen URL-címet kapni egy blobhoz az Azure-tárban: használjon olyan MEGOSZTOTT hozzáférés-aláírást (SAS), amely olvasási engedélyeket ad a blobhoz, vagy állítsa be a blob vagy tároló ACL-jét a nyilvános hozzáférés engedélyezése érdekében.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
A blobtároló URL-címe az Azure Blob Storage-ban.
Ennek az URL-címnek olvashatónak és listolhatónak kell lennie névtelen hozzáféréssel; azaz a Batch szolgáltatás nem ad meg hitelesítő adatokat, amikor blobokat tölt le a tárolóból.
Kétféleképpen állíthat be ilyen URL-címet egy Azure-tárban található tárolóhoz: egy olyan MEGOSZTOTT hozzáférés-aláírást (SAS), amely olvasási engedélyeket ad a tárolóhoz, vagy úgy állíthatja be a tároló ACL-jét, hogy engedélyezze a nyilvános hozzáférést.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Bat. Models.PSResourceFile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzBatchTask](./New-AzBatchTask.md)