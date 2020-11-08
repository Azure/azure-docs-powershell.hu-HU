---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182600"
---
# New-AzBatchResourceFile

## Áttekintés
Létrehoz egy erőforrást a felhasználáshoz `New-AzBatchTask` .

## SZINTAXISA

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

## Leírás
Létrehoz egy erőforrást a felhasználáshoz `New-AzBatchTask` .

## Példák

### Példa 1: erőforrásfájl létrehozása egy, a HTTP URL-címéről egyetlen fájlra mutatva
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`Http-URL-címre hivatkozó hivatkozás létrehozása

### 2. példa: erőforrásfájl létrehozása Azure Storage Container URL-címről
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`Az Azure Storage Container URL-jének hivatkozását hozza létre. A program a tárolóban lévő összes fájlt letölti a megadott mappába.

### 3. példa: erőforrásfájl létrehozása automatikus tárterület-tároló nevében
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Létrehozza `PSResourceFile` az automatikus tárterület-tároló neve hivatkozását. A program a tárolóban lévő összes fájlt letölti a megadott mappába.

## PARAMÉTEREK

### -AutoStorageContainerName
A tároló tároló neve az automatikus tárterület-fiókban.

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
Az Azure-tárterületről való letöltéskor használandó blob-előtagot kapja.
A program csak azokat a festékfoltok-t tölti le, amelyek nevei a megadott előtaggal kezdődnek.
Ez az előtag lehet részleges fájlnév vagy alkönyvtár.
Ha nem adja meg az előtagot, a program a tárolóban lévő összes fájlt letölti.

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
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A fájl jogosultsági mód attribútumát oktális formátumban kapja meg.
Ez a tulajdonság csak akkor érvényes, ha az erőforrást egy Linux-csomópontra tölti le.
Ha a tulajdonság nem egy Linux-csomóponthoz van megadva, az alapértelmezett érték az 0770.

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
A számítási csomópont azon helye, amelyre a fájl (ok) letöltése a tevékenység munkakönyvtárához viszonyítva. Ha a HttpUrl paramétert adja meg, a FilePath szükséges, és leírja, hogy a fájl milyen elérési utat fog letölteni, például a fájlnevet. Ellenkező esetben, ha a AutoStorageContainerName vagy a StorageContainerUrl paraméter van megadva, a FilePath nem kötelező, és a címtár a fájlok letöltéséhez. Abban az esetben, ha a FilePath címtárként használja, a bemeneti adatokhoz társított bármely címtár-szerkezet teljes egészében megmarad, és a program hozzáfűzi a megadott FilePath-könyvtárhoz. A megadott relatív elérési út nem szünteti meg a tevékenység munkakönyvtárát (például: "...").

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
A letöltendő fájl URL-címe.
Ha az URL-cím az Azure Blob-tároló, akkor a névtelen hozzáférés szolgáltatással olvashatónak kell lennie; vagyis a köteg szolgáltatás nem jelent meg hitelesítő adatokat a blob letöltésekor.
Az Azure Storage szolgáltatásban kétféleképpen lehet egy blob-URL-címet beolvasni: az olvasási engedélyeket biztosító megosztott hozzáférés-aláírás (SAS), illetve a blob vagy a tárolója HOZZÁFÉRÉSének beállítása a nyilvános hozzáférés engedélyezéséhez.

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
A blob-tároló URL-címe az Azure Blob-tárterületen belül.
Ennek az URL-címnek olvashatónak és olvashatónak kell lennie a névtelen hozzáférés használatával; vagyis a köteg szolgáltatás nem jelent meg hitelesítő adatokat a tárolóból való letöltéskor.
Az Azure-tárterületen lévő tárolók esetében kétféle módon lehet URL-t beolvasni: egy megosztott hozzáférés-aláírást (SAS) kell megadni, amely olvasási engedélyeket ad a tárolónak, vagy a tároló hozzáférés-vezérlési listáját a nyilvános hozzáférés engedélyezéséhez adja meg.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSResourceFile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzBatchTask](./New-AzBatchTask.md)