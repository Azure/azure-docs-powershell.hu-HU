---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366699"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
A rendszer és az Azure File Sync közötti esetleges kompatibilitási problémákat ellenőrzi.

## SZINTAXIS

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

## LEÍRÁS
Az **Invoke-AzStorageSyncCompatibilityCheck** parancsmag ellenőrzi a rendszer és az Azure File Sync közötti esetleges kompatibilitási problémákat. Egy helyi vagy távoli elérési út megadva érvényesíti a rendszert és a fájlnévteret, majd visszaadja a talált kompatibilitási problémákat.
Rendszerellenőrzések:
- Az operációs rendszer kompatibilitási fájlnévterének ellenőrzése:
- Nem támogatott karakterek
- Maximális fájlméret
- Maximális elérési út hossza
- Fájl maximális hossza
- Az adatkészlet maximális mérete
- Címtár mélységének maximális mérete

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Ez a parancs ellenőrzi a rendszer, valamint a C:\DATA fájlokkal és mappákkal való kompatibilitását.

### 2. példa
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Ez a parancs ellenőrzi a C:\DATA fájlokkal és mappákkal való kompatibilitást, de nem ellenőrzi a rendszer kompatibilitását.

### 3. példa
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Ez a parancs ellenőrzi a rendszer, valamint a C:\DATA fájlokkal és mappákkal való kompatibilitását, majd az eredményeket CSV-fájlként exportálja a C:\results fájlba.

## PARAMETERS

### -ComputerName
Az a számítógép, amely ezt az ellenőrzést végzi.

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
Az érvényesíthető megosztás hitelesítő adatai.

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

### -Path
Az érvényesített megosztás UNC elérési útja.

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
Ezt a jelölőt beállítva kihagyhatja a fájlnévtér-érvényesítéseket, és csak rendszerérvényesítéseket hajthat végre.

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
Ezt a jelölőt beállítva kihagyhatja a rendszerérvényesítéseket, és csak a fájlnévtér-érvényesítéseket hajthatja végre.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## MEGJEGYZÉSEK
* Kulcsszavak: azure, Az, arm, erőforrás, kezelés, tárhelyszinkronizáció, fájlszinkronizáció

## KAPCSOLÓDÓ HIVATKOZÁSOK
