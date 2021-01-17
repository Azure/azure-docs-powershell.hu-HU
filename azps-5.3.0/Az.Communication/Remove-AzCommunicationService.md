---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480912"
---
# <span data-ttu-id="4d787-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="4d787-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="4d787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d787-102">SYNOPSIS</span></span>
<span data-ttu-id="4d787-103">Művelet a CommunicationService törléséhez.</span><span class="sxs-lookup"><span data-stu-id="4d787-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="4d787-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d787-104">SYNTAX</span></span>

### <span data-ttu-id="4d787-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d787-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d787-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d787-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d787-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d787-107">DESCRIPTION</span></span>
<span data-ttu-id="4d787-108">Művelet a CommunicationService törléséhez.</span><span class="sxs-lookup"><span data-stu-id="4d787-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="4d787-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d787-109">EXAMPLES</span></span>

### <span data-ttu-id="4d787-110">1. példa: A megadott Azure Communication-erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4d787-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="4d787-111">Távolítsa el/törölje az Azure Communication erőforrást.</span><span class="sxs-lookup"><span data-stu-id="4d787-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="4d787-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d787-112">PARAMETERS</span></span>

### <span data-ttu-id="4d787-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d787-113">-AsJob</span></span>
<span data-ttu-id="4d787-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="4d787-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4d787-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d787-115">-DefaultProfile</span></span>
<span data-ttu-id="4d787-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d787-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d787-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d787-117">-InputObject</span></span>
<span data-ttu-id="4d787-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4d787-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d787-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4d787-119">-Name</span></span>
<span data-ttu-id="4d787-120">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4d787-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d787-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4d787-121">-NoWait</span></span>
<span data-ttu-id="4d787-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="4d787-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4d787-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d787-123">-PassThru</span></span>
<span data-ttu-id="4d787-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="4d787-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4d787-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d787-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d787-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d787-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4d787-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="4d787-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4d787-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d787-128">-SubscriptionId</span></span>
<span data-ttu-id="4d787-129">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4d787-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4d787-130">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4d787-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4d787-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d787-131">-Confirm</span></span>
<span data-ttu-id="4d787-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4d787-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d787-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d787-133">-WhatIf</span></span>
<span data-ttu-id="4d787-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4d787-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d787-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d787-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d787-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d787-136">CommonParameters</span></span>
<span data-ttu-id="4d787-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d787-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d787-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d787-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d787-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d787-139">INPUTS</span></span>

### <span data-ttu-id="4d787-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="4d787-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="4d787-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d787-141">OUTPUTS</span></span>

### <span data-ttu-id="4d787-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d787-142">System.Boolean</span></span>

## <span data-ttu-id="4d787-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d787-143">NOTES</span></span>

<span data-ttu-id="4d787-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4d787-144">ALIASES</span></span>

<span data-ttu-id="4d787-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4d787-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d787-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4d787-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d787-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d787-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d787-148">INPUTOBJECT: <ICommunicationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4d787-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d787-149">`[CommunicationServiceName <String>]`: A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4d787-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="4d787-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4d787-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d787-151">`[Location <String>]`: Az Azure régió</span><span class="sxs-lookup"><span data-stu-id="4d787-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="4d787-152">`[OperationId <String>]`: Folyamatban lévő async-művelet azonosítója</span><span class="sxs-lookup"><span data-stu-id="4d787-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="4d787-153">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d787-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4d787-154">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="4d787-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4d787-155">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4d787-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="4d787-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4d787-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4d787-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d787-157">RELATED LINKS</span></span>

