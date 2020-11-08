---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182215"
---
# <span data-ttu-id="a97bd-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="a97bd-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="a97bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a97bd-102">SYNOPSIS</span></span>
<span data-ttu-id="a97bd-103">Egy meglévő feladat törlése</span><span class="sxs-lookup"><span data-stu-id="a97bd-103">Deletes an existing job.</span></span>
<span data-ttu-id="a97bd-104">Csak a létrehozó vagy a Befejezett állapotú feladatok törölhetők.</span><span class="sxs-lookup"><span data-stu-id="a97bd-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="a97bd-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a97bd-105">SYNTAX</span></span>

### <span data-ttu-id="a97bd-106">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a97bd-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a97bd-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a97bd-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a97bd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a97bd-108">DESCRIPTION</span></span>
<span data-ttu-id="a97bd-109">Egy meglévő feladat törlése</span><span class="sxs-lookup"><span data-stu-id="a97bd-109">Deletes an existing job.</span></span>
<span data-ttu-id="a97bd-110">Csak a létrehozó vagy a Befejezett állapotú feladatok törölhetők.</span><span class="sxs-lookup"><span data-stu-id="a97bd-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="a97bd-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a97bd-111">EXAMPLES</span></span>

### <span data-ttu-id="a97bd-112">1. példa: a ImportExport-feladat eltávolítása a resourceGroup és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="a97bd-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="a97bd-113">Ez a parancsmag eltávolítja a ImportExport-feladatot a resourceGroup és a kiszolgáló neve alapján.</span><span class="sxs-lookup"><span data-stu-id="a97bd-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="a97bd-114">2. példa: ImportExport feladat eltávolítása identitással</span><span class="sxs-lookup"><span data-stu-id="a97bd-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="a97bd-115">Ezek a parancsmagok a ImportExport-feladatot identitással távolítják el.</span><span class="sxs-lookup"><span data-stu-id="a97bd-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="a97bd-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a97bd-116">PARAMETERS</span></span>

### <span data-ttu-id="a97bd-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="a97bd-117">-AcceptLanguage</span></span>
<span data-ttu-id="a97bd-118">A válasz kívánt nyelvét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a97bd-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="a97bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97bd-119">-DefaultProfile</span></span>
<span data-ttu-id="a97bd-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a97bd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a97bd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a97bd-121">-InputObject</span></span>
<span data-ttu-id="a97bd-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a97bd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a97bd-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a97bd-123">-Name</span></span>
<span data-ttu-id="a97bd-124">Az Importálás/exportálás feladat neve.</span><span class="sxs-lookup"><span data-stu-id="a97bd-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="a97bd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a97bd-125">-PassThru</span></span>
<span data-ttu-id="a97bd-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="a97bd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a97bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="a97bd-128">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a97bd-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="a97bd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a97bd-129">-SubscriptionId</span></span>
<span data-ttu-id="a97bd-130">Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a97bd-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="a97bd-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a97bd-131">-Confirm</span></span>
<span data-ttu-id="a97bd-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a97bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a97bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a97bd-133">-WhatIf</span></span>
<span data-ttu-id="a97bd-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a97bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a97bd-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a97bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a97bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97bd-136">CommonParameters</span></span>
<span data-ttu-id="a97bd-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a97bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97bd-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a97bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97bd-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a97bd-139">INPUTS</span></span>

### <span data-ttu-id="a97bd-140">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="a97bd-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="a97bd-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a97bd-141">OUTPUTS</span></span>

### <span data-ttu-id="a97bd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a97bd-142">System.Boolean</span></span>

## <span data-ttu-id="a97bd-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a97bd-143">NOTES</span></span>

<span data-ttu-id="a97bd-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a97bd-144">ALIASES</span></span>

<span data-ttu-id="a97bd-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a97bd-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a97bd-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a97bd-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a97bd-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a97bd-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a97bd-148">INPUTOBJECT <IImportExportIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a97bd-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a97bd-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a97bd-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a97bd-150">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="a97bd-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="a97bd-151">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="a97bd-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="a97bd-152">Például Nyugat-amerikai vagy westus.</span><span class="sxs-lookup"><span data-stu-id="a97bd-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="a97bd-153">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a97bd-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="a97bd-154">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a97bd-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="a97bd-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a97bd-155">RELATED LINKS</span></span>

