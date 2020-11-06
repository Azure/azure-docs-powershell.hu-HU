---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 84192a4715087d5ae896067e02ab07ef27574410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492100"
---
# Set-AzureStorageFileContent

## Áttekintés
Feltölti a fájl tartalmát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Megosztásnév (alapértelmezett)
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Megosztása
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Directory
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **set-AzureStorageFileContent** parancsmag a fájl tartalmát egy megadott megosztásban lévő fájlba tölti fel.

## Példák

### 1. példa: fájl feltöltése az aktuális mappában
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

A parancs feltölti a DataFile37 nevű fájlt az aktuális mappában egy CurrentDataFile nevű fájlként a ContosoWorkingFolder nevű mappában.

### 2. példa: az aktuális mappa összes fájljának feltöltése
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

Ez a példa számos gyakori Windows PowerShell-parancsmagot és a jelenlegi parancsmagot használ, így az aktuális mappából az összes fájlt feltöltheti a tároló ContosoShare06 gyökérkönyvtárába.
Az első parancs megkapja az aktuális mappa nevét, és a $CurrentFolder változóban tárolja.
A második parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beszerzéséhez, majd a $Container változóban tárolja.
A végleges parancs beolvassa az aktuális mappa tartalmát, és átadja őket az Where-Object parancsmagnak a pipeline operátor használatával.
Ez a parancsmag kiszűri a fájlokat nem tartalmazó objektumokat, majd átadja a fájlokat az ForEach-Object parancsmagnak.
A parancsmag minden olyan fájlhoz parancsfájl-zárolást futtat, amely a megfelelő elérési utat hozza létre, majd az aktuális parancsmagot használja a fájl feltöltéséhez.
Az eredmény ugyanazt a nevet és relatív pozíciót veszi figyelembe az egyéb, a példa által feltöltött fájlokkal kapcsolatban.
A parancsfájl-blokkokról a következő témakörben olvashat bővebben: `Get-Help about_Script_Blocks`

## PARAMÉTEREK

### -ClientTimeoutPerRequest
Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.
Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.
Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.

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

### -ConcurrentTaskCount
A párhuzamos hálózati hívásokat adja meg.
Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.
A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.
Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).
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
Az Azure tárolási környezetét adja meg.
A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.

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
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címtár
**CloudFileDirectory** -objektumként adja meg a mappát.
Ez a parancsmag feltölti a fájlt a paraméter által megadott mappába.
Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.
A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Jelzi, hogy ez a parancsmag felülír egy meglévő Azure-tárterületet.

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
Azt jelzi, hogy ez a parancsmag az általa létrehozott vagy feltöltött **AzureStorageFile** objektumot adja eredményül.

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

### -Path (elérési út)
A fájl vagy mappa elérési útját adja meg.
Ezzel a parancsmaggal a program feltölti a tartalmat a paraméter által megadott fájlba vagy a paraméter által megadott mappában lévő fájlba.
Ha megad egy mappát, a parancsmag a forrásfájl nevével megegyező nevű fájlt hoz létre.
Ha olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat.
Ha olyan fájlt ad meg, amely már létezik, és az _erő_ paramétert adja meg, ez a parancsmag felülírja a fájl tartalmát.
Ha olyan fájlt ad meg, amely már létezik, és nem adja meg az _erő_ lehetőséget, ez a parancsmag nem változtatja meg, és hibát ad eredményül.
Ha olyan mappa elérési útját adja meg, amely nem létezik, akkor ez a parancsmag nem változtatja meg a hibát, és hibát jelez.

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

### -ServerTimeoutPerRequest
A kérés kiszolgálói részének időtúllépési időszakát adja meg.

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

### -Share (megosztás)
Egy **CloudFileShare** -objektumot ad meg.
Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.
**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.
Ez az objektum a tárolási környezetet tartalmazza.
Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Megosztásnév
Itt adhatja meg a fájl megosztásának a nevét.
Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.

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

### -Forrás
A parancsmag által feltöltött forrásfájlt adja meg.
Ha olyan fájlt ad meg, amely nem létezik, a parancsmag hibát jelez.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Storage. file. CloudFileShare
Paraméterek: Share (ByValue)

### Microsoft. WindowsAzure. Storage. file. CloudFileDirectory
Paraméterek: címtár (ByValue)

### System. String

### Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext

## KIMENETEK

### Microsoft. WindowsAzure. Storage. file. CloudFile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[Új – AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)
