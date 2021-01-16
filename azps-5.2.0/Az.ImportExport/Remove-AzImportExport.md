---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364501"
---
# <span data-ttu-id="c4f54-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="c4f54-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="c4f54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4f54-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f54-103">Töröl egy meglévő feladatot.</span><span class="sxs-lookup"><span data-stu-id="c4f54-103">Deletes an existing job.</span></span>
<span data-ttu-id="c4f54-104">Csak a Létrehozás vagy a Befejezve államban törölt feladatok törölhetők.</span><span class="sxs-lookup"><span data-stu-id="c4f54-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="c4f54-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4f54-105">SYNTAX</span></span>

### <span data-ttu-id="c4f54-106">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4f54-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4f54-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4f54-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4f54-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4f54-108">DESCRIPTION</span></span>
<span data-ttu-id="c4f54-109">Töröl egy meglévő feladatot.</span><span class="sxs-lookup"><span data-stu-id="c4f54-109">Deletes an existing job.</span></span>
<span data-ttu-id="c4f54-110">Csak a Létrehozás vagy a Befejezve államban törölt feladatok törölhetők.</span><span class="sxs-lookup"><span data-stu-id="c4f54-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="c4f54-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4f54-111">EXAMPLES</span></span>

### <span data-ttu-id="c4f54-112">1. példa: Az ImportExport feladat eltávolítása erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="c4f54-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="c4f54-113">Ez a parancsmag eltávolítja az ImportExport feladatot az resourceGroup és a kiszolgáló neve alapján.</span><span class="sxs-lookup"><span data-stu-id="c4f54-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="c4f54-114">2. példa: Az ImportExport feladat eltávolítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="c4f54-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="c4f54-115">Ezek a parancsmagok identitás szerint eltávolítják az ImportExport feladatot.</span><span class="sxs-lookup"><span data-stu-id="c4f54-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="c4f54-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4f54-116">PARAMETERS</span></span>

### <span data-ttu-id="c4f54-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="c4f54-117">-AcceptLanguage</span></span>
<span data-ttu-id="c4f54-118">A válasz elsődleges nyelvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c4f54-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="c4f54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f54-119">-DefaultProfile</span></span>
<span data-ttu-id="c4f54-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4f54-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4f54-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4f54-121">-InputObject</span></span>
<span data-ttu-id="c4f54-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c4f54-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4f54-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c4f54-123">-Name</span></span>
<span data-ttu-id="c4f54-124">Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="c4f54-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f54-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4f54-125">-PassThru</span></span>
<span data-ttu-id="c4f54-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="c4f54-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4f54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f54-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4f54-128">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="c4f54-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f54-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4f54-129">-SubscriptionId</span></span>
<span data-ttu-id="c4f54-130">Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4f54-130">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f54-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4f54-131">-Confirm</span></span>
<span data-ttu-id="c4f54-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c4f54-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f54-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4f54-133">-WhatIf</span></span>
<span data-ttu-id="c4f54-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c4f54-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4f54-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4f54-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f54-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f54-136">CommonParameters</span></span>
<span data-ttu-id="c4f54-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f54-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f54-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4f54-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f54-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4f54-139">INPUTS</span></span>

### <span data-ttu-id="c4f54-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="c4f54-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="c4f54-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4f54-141">OUTPUTS</span></span>

### <span data-ttu-id="c4f54-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4f54-142">System.Boolean</span></span>

## <span data-ttu-id="c4f54-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4f54-143">NOTES</span></span>

<span data-ttu-id="c4f54-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c4f54-144">ALIASES</span></span>

<span data-ttu-id="c4f54-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c4f54-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4f54-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c4f54-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4f54-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4f54-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4f54-148">INPUTOBJECT: <IImportExportIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c4f54-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4f54-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c4f54-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4f54-150">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="c4f54-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="c4f54-151">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="c4f54-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="c4f54-152">Ilyen például az Egyesült Államok nyugati és nyugati régiója.</span><span class="sxs-lookup"><span data-stu-id="c4f54-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="c4f54-153">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="c4f54-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="c4f54-154">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4f54-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="c4f54-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4f54-155">RELATED LINKS</span></span>

