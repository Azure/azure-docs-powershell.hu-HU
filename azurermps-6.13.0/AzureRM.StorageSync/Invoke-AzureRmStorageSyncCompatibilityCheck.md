---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498127"
---
# Invoke-AzureRmStorageSyncCompatibilityCheck

## Áttekintés
Ellenőrzi, hogy milyen kompatibilitási problémákat tapasztal a rendszer és az Azure-fájlok szinkronizálása között.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### PathBased (alapértelmezett)
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## Leírás
A **meghívó-AzureRmStorageSyncCompatibilityCheck** parancsmag a rendszer és az Azure-fájlok szinkronizálása közötti esetleges kompatibilitási problémákat ellenőrzi. Helyi vagy távoli elérési út esetén az érvényes beállításokat a rendszer és a fájl névtérben hajtja végre, majd a talált kompatibilitási problémákat adja eredményül.
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
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

Ez a parancs ellenőrzi a rendszer és a fájlok és mappák kompatibilitását a C:\DATA.-ban.

### 2. példa
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Ez a parancs ellenőrzi a fájlok és mappák kompatibilitását a C:\ADATOK-ban, de nem végez rendszerkompatibilitás-ellenőrzést.

### 3. példa
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
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

### -Quiet (csendes)
Letiltja a kimeneti jelentés írását a konzolra.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. StorageSync. Értékelés. modellek. PSValidationResult

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, storagesync, filesync

## KAPCSOLÓDÓ HIVATKOZÁSOK
