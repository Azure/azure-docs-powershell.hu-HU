---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: 3feb6e2246e2265c36e67d64621a5726eaabb6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938930"
---
# <span data-ttu-id="795e1-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="795e1-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="795e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="795e1-102">SYNOPSIS</span></span>
<span data-ttu-id="795e1-103">Művelet a CommunicationService törléséhez.</span><span class="sxs-lookup"><span data-stu-id="795e1-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="795e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="795e1-104">SYNTAX</span></span>

### <span data-ttu-id="795e1-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="795e1-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="795e1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="795e1-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="795e1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="795e1-107">DESCRIPTION</span></span>
<span data-ttu-id="795e1-108">Művelet a CommunicationService törléséhez.</span><span class="sxs-lookup"><span data-stu-id="795e1-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="795e1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="795e1-109">EXAMPLES</span></span>

### <span data-ttu-id="795e1-110">1. példa: A megadott Azure Communication-erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="795e1-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="795e1-111">Távolítsa el/törölje az Azure Communication erőforrást.</span><span class="sxs-lookup"><span data-stu-id="795e1-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="795e1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="795e1-112">PARAMETERS</span></span>

### <span data-ttu-id="795e1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="795e1-113">-AsJob</span></span>
<span data-ttu-id="795e1-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="795e1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="795e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795e1-115">-DefaultProfile</span></span>
<span data-ttu-id="795e1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="795e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="795e1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="795e1-117">-InputObject</span></span>
<span data-ttu-id="795e1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="795e1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="795e1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="795e1-119">-Name</span></span>
<span data-ttu-id="795e1-120">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="795e1-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="795e1-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="795e1-121">-NoWait</span></span>
<span data-ttu-id="795e1-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="795e1-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="795e1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="795e1-123">-PassThru</span></span>
<span data-ttu-id="795e1-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="795e1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="795e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="795e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="795e1-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="795e1-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="795e1-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="795e1-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="795e1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="795e1-128">-SubscriptionId</span></span>
<span data-ttu-id="795e1-129">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="795e1-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="795e1-130">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="795e1-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="795e1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="795e1-131">-Confirm</span></span>
<span data-ttu-id="795e1-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="795e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="795e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="795e1-133">-WhatIf</span></span>
<span data-ttu-id="795e1-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="795e1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="795e1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="795e1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="795e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795e1-136">CommonParameters</span></span>
<span data-ttu-id="795e1-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795e1-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="795e1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795e1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="795e1-139">INPUTS</span></span>

### <span data-ttu-id="795e1-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="795e1-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="795e1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="795e1-141">OUTPUTS</span></span>

### <span data-ttu-id="795e1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="795e1-142">System.Boolean</span></span>

## <span data-ttu-id="795e1-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="795e1-143">NOTES</span></span>

<span data-ttu-id="795e1-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="795e1-144">ALIASES</span></span>

<span data-ttu-id="795e1-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="795e1-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="795e1-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="795e1-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="795e1-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="795e1-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="795e1-148">INPUTOBJECT: <ICommunicationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="795e1-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="795e1-149">`[CommunicationServiceName <String>]`: A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="795e1-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="795e1-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="795e1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="795e1-151">`[Location <String>]`: Az Azure régió</span><span class="sxs-lookup"><span data-stu-id="795e1-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="795e1-152">`[OperationId <String>]`: Folyamatban lévő async-művelet azonosítója</span><span class="sxs-lookup"><span data-stu-id="795e1-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="795e1-153">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="795e1-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="795e1-154">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="795e1-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="795e1-155">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="795e1-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="795e1-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="795e1-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="795e1-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="795e1-157">RELATED LINKS</span></span>

