---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183783"
---
# Invoke-AzStorageSyncCompatibilityCheck

## Áttekintés
Ellenőrzi, hogy milyen kompatibilitási problémákat tapasztal a rendszer és az Azure-fájlok szinkronizálása között.

## SZINTAXISA

### PathBased (alapértelmezett)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## Leírás
A **meghívó-AzStorageSyncCompatibilityCheck** parancsmag a rendszer és az Azure-fájlok szinkronizálása közötti esetleges kompatibilitási problémákat ellenőrzi. Helyi vagy távoli elérési út esetén az érvényes beállításokat a rendszer és a fájl névtérben hajtja végre, majd a talált kompatibilitási problémákat adja eredményül.
Rendszerellenőrzések:
- Az operációs rendszer kompatibilitási fájljának névtér-ellenőrzése:
- Nem támogatott karakterek
- Maximális fájlméret
- Maximális útvonal hossza
- Fájl maximális hossza
- Adatkészlet maximális mérete
- A könyvtár maximális mélysége

## Példák

### Példa 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Ez a parancs ellenőrzi a rendszer és a fájlok és mappák kompatibilitását a C:\DATA.-ban.

### 2. példa
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Ez a parancs ellenőrzi a fájlok és mappák kompatibilitását a C:\ADATOK-ban, de nem végez rendszerkompatibilitás-ellenőrzést.

### 3. példa
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Ez a parancs ellenőrzi a rendszer és a fájlok és mappák kompatibilitását a C:\ADATOK-ban, majd CSV-fájlként exportálja az eredményeket a C:\results.

## PARAMÉTEREK

### -Számítógépnév
Az a számítógép, amelyen a beadást végrehajtja.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítő adatok
Az érvényesíteni kívánt megosztáshoz tartozó hitelesítő adatok.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
Az érvényesíteni kívánt megosztás UNC-elérési útja.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNamespaceChecks
Ezt a jelölőt úgy állíthatja be, hogy kihagyja a fájl névterének érvényességét, és csak a rendszerérvényességet végezze

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
Ezt a jelölőt beállíthatja a rendszerérvényességek kihagyására, és csak a fájl névterének érvényességét végezze el.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. StorageSync. Értékelés. modellek. PSValidationResult

## MEGJEGYZI
* Kulcsszavak: Azure, az, kar, erőforrás, kezelés, storagesync, filesync

## KAPCSOLÓDÓ HIVATKOZÁSOK
