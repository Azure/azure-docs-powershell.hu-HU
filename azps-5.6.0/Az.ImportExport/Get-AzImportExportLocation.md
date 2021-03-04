---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: 928ac0254619a2924421a0b52bf20212b8ba19a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924106"
---
# Get-AzImportExportLocation

## SYNOPSIS
Az importálási vagy exportálási feladathoz társított lemezeket tartalmazó hely adatait adja vissza.
A hely egy Azure-régió.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
Az importálási vagy exportálási feladathoz társított lemezeket tartalmazó hely adatait adja vissza.
A hely egy Azure-régió.

## PÉLDÁK

### 1. példa: Az Összes Azure-régió helyének részleteinek lekérte az alapértelmezett környezetben
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

Ez a parancsmag az összes Azure-régió helyének adatait bekérte az alapértelmezett környezetben.

### 2. példa: Azure-régió helyének részletei hely neve alapján
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Ez a parancsmag helynév szerint lekérte az Azure-régió adatait.

### 3. példa: Azure-régió tartózkodási helyének lekért részletei identitás alapján
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Ez a parancsmaglista identitás alapján lekérte az Azure-régió helyének részleteit.

## PARAMETERS

### -AcceptLanguage
A válasz elsődleges nyelvét határozza meg.

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

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A hely neve.
Ilyen például az Egyesült Államok nyugati és nyugati régiója.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IImportExportIdentity> Identity Parameter
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[JobName <String>]`: Az importálási/exportálási feladat neve.
  - `[LocationName <String>]`: A hely neve. Ilyen például az Egyesült Államok nyugati és nyugati régiója.
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.
  - `[SubscriptionId <String>]`: Az Azure-felhasználó előfizetésazonosítója.

## KAPCSOLÓDÓ HIVATKOZÁSOK

