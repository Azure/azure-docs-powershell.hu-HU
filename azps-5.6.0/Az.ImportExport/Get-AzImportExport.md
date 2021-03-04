---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 8825cb9b3d4a2efcd6a326244139950e431d71f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924930"
---
# Get-AzImportExport

## SYNOPSIS
Információkat kap egy meglévő feladatról.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Lista1
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
Információkat kap egy meglévő feladatról.

## PÉLDÁK

### 1. példa: Az Importálásexportálás feladat lekérte az alapértelmezett környezetben
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Ez a parancsmag importálásiexportált feladatot kap alapértelmezett környezetben.

### 2. példa: Az ImportExport feladat lekérte erőforráscsoport és feladat neve szerint
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Ez a parancsmag az ImportExport feladatot erőforráscsoport és a feladat neve alapján kapja meg.

### 3. példa: A megadott erőforráscsoportban található ImportExport feladatok listája
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Ez a parancsmag felsorolja a megadott erőforráscsoportban található ImportExport feladatokat.

### 4. példa: ImportExport feladat lekérte identitás szerint
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Ez a parancsmaglista identitás alapján importálja az ImportExport feladatot.

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

### -Filter
Az eredmények adott feltételekre való korlátozására használhatók.

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

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
Az importálási/exportálási feladat neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az Azure-felhasználó előfizetésazonosítója.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Egész szám, amely azt adja meg, hogy a visszaadott feladatok közül hány legyen a legnagyobb.
Az érték nem haladhatja meg a 100-as értéket.

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
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

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse

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

