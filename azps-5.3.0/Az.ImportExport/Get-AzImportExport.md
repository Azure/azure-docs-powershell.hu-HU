---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480278"
---
# <span data-ttu-id="ee1ac-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="ee1ac-101">Get-AzImportExport</span></span>

## <span data-ttu-id="ee1ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1ac-103">Információkat kap egy meglévő feladatról.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="ee1ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee1ac-104">SYNTAX</span></span>

### <span data-ttu-id="ee1ac-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee1ac-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee1ac-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="ee1ac-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee1ac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee1ac-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee1ac-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="ee1ac-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ee1ac-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee1ac-109">DESCRIPTION</span></span>
<span data-ttu-id="ee1ac-110">Információkat kap egy meglévő feladatról.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="ee1ac-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee1ac-111">EXAMPLES</span></span>

### <span data-ttu-id="ee1ac-112">1. példa: Az Importálásexportálás feladat lekérte az alapértelmezett környezetben</span><span class="sxs-lookup"><span data-stu-id="ee1ac-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ee1ac-113">Ez a parancsmag importálásiexportált feladatot kap alapértelmezett környezetben.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="ee1ac-114">2. példa: Az ImportExport feladat lekérte erőforráscsoport és feladat neve szerint</span><span class="sxs-lookup"><span data-stu-id="ee1ac-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ee1ac-115">Ez a parancsmag az ImportExport feladatot erőforráscsoport és a feladat neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="ee1ac-116">3. példa: A megadott erőforráscsoportban található ImportExport feladatok listája</span><span class="sxs-lookup"><span data-stu-id="ee1ac-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ee1ac-117">Ez a parancsmag felsorolja a megadott erőforráscsoportban található ImportExport feladatokat.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="ee1ac-118">4. példa: Az ImportExport feladat lekérte identitás szerint</span><span class="sxs-lookup"><span data-stu-id="ee1ac-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ee1ac-119">Ez a parancsmaglista identitás alapján importálja az ImportExport feladatot.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="ee1ac-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee1ac-120">PARAMETERS</span></span>

### <span data-ttu-id="ee1ac-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ee1ac-121">-AcceptLanguage</span></span>
<span data-ttu-id="ee1ac-122">A válasz elsődleges nyelvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="ee1ac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1ac-123">-DefaultProfile</span></span>
<span data-ttu-id="ee1ac-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1ac-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="ee1ac-125">-Filter</span></span>
<span data-ttu-id="ee1ac-126">Az eredmények adott feltételekre való korlátozására használhatók.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="ee1ac-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee1ac-127">-InputObject</span></span>
<span data-ttu-id="ee1ac-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee1ac-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ee1ac-129">-Name</span></span>
<span data-ttu-id="ee1ac-130">Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="ee1ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="ee1ac-132">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="ee1ac-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee1ac-133">-SubscriptionId</span></span>
<span data-ttu-id="ee1ac-134">Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="ee1ac-135">-Top</span><span class="sxs-lookup"><span data-stu-id="ee1ac-135">-Top</span></span>
<span data-ttu-id="ee1ac-136">Egész szám, amely azt adja meg, hogy a visszaadott feladatok közül hány legyen a legnagyobb.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="ee1ac-137">Az érték nem haladhatja meg a 100-as értéket.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="ee1ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1ac-138">CommonParameters</span></span>
<span data-ttu-id="ee1ac-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1ac-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee1ac-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1ac-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee1ac-141">INPUTS</span></span>

### <span data-ttu-id="ee1ac-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="ee1ac-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="ee1ac-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee1ac-143">OUTPUTS</span></span>

### <span data-ttu-id="ee1ac-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="ee1ac-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="ee1ac-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee1ac-145">NOTES</span></span>

<span data-ttu-id="ee1ac-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ee1ac-146">ALIASES</span></span>

<span data-ttu-id="ee1ac-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ee1ac-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee1ac-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee1ac-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee1ac-150">INPUTOBJECT: <IImportExportIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ee1ac-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee1ac-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ee1ac-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee1ac-152">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="ee1ac-153">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="ee1ac-154">Ilyen például az Egyesült Államok nyugati és nyugati régiója.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="ee1ac-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="ee1ac-156">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee1ac-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="ee1ac-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee1ac-157">RELATED LINKS</span></span>

