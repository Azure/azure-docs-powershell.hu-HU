---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351977"
---
# <span data-ttu-id="351ed-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="351ed-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="351ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="351ed-102">SYNOPSIS</span></span>
<span data-ttu-id="351ed-103">Egy meglévő egyéni erőforrás-szolgáltató frissítése.</span><span class="sxs-lookup"><span data-stu-id="351ed-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="351ed-104">A PATCH-en keresztül jelenleg csak a címkék frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="351ed-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="351ed-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="351ed-105">SYNTAX</span></span>

### <span data-ttu-id="351ed-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="351ed-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="351ed-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="351ed-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="351ed-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="351ed-108">DESCRIPTION</span></span>
<span data-ttu-id="351ed-109">Egy meglévő egyéni erőforrás-szolgáltató frissítése.</span><span class="sxs-lookup"><span data-stu-id="351ed-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="351ed-110">A PATCH-en keresztül jelenleg csak a címkék frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="351ed-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="351ed-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="351ed-111">EXAMPLES</span></span>

### <span data-ttu-id="351ed-112">1. példa: Címkék hozzáadása egyéni szolgáltatóhoz</span><span class="sxs-lookup"><span data-stu-id="351ed-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="351ed-113">Frissítse egy egyéni szolgáltató címkéit.</span><span class="sxs-lookup"><span data-stu-id="351ed-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="351ed-114">2. példa: Egyéni szolgáltató frissítése pipázással</span><span class="sxs-lookup"><span data-stu-id="351ed-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="351ed-115">Egyéni szolgáltató frissítése pipázás használatával.</span><span class="sxs-lookup"><span data-stu-id="351ed-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="351ed-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="351ed-116">PARAMETERS</span></span>

### <span data-ttu-id="351ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351ed-117">-DefaultProfile</span></span>
<span data-ttu-id="351ed-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="351ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="351ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="351ed-119">-InputObject</span></span>
<span data-ttu-id="351ed-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="351ed-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="351ed-121">-Name</span><span class="sxs-lookup"><span data-stu-id="351ed-121">-Name</span></span>
<span data-ttu-id="351ed-122">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="351ed-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="351ed-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="351ed-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351ed-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="351ed-125">-SubscriptionId</span></span>
<span data-ttu-id="351ed-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="351ed-126">The Azure subscription ID.</span></span>
<span data-ttu-id="351ed-127">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="351ed-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351ed-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="351ed-128">-Tag</span></span>
<span data-ttu-id="351ed-129">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="351ed-129">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351ed-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="351ed-130">-Confirm</span></span>
<span data-ttu-id="351ed-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="351ed-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="351ed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="351ed-132">-WhatIf</span></span>
<span data-ttu-id="351ed-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="351ed-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="351ed-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="351ed-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="351ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351ed-135">CommonParameters</span></span>
<span data-ttu-id="351ed-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="351ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351ed-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="351ed-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351ed-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="351ed-138">INPUTS</span></span>

### <span data-ttu-id="351ed-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="351ed-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="351ed-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="351ed-140">OUTPUTS</span></span>

### <span data-ttu-id="351ed-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="351ed-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="351ed-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="351ed-142">NOTES</span></span>

<span data-ttu-id="351ed-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="351ed-143">ALIASES</span></span>

<span data-ttu-id="351ed-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="351ed-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="351ed-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="351ed-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="351ed-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="351ed-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="351ed-147">INPUTOBJECT: <ICustomProvidersIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="351ed-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="351ed-148">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="351ed-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="351ed-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="351ed-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="351ed-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="351ed-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="351ed-151">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="351ed-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="351ed-152">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="351ed-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="351ed-153">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="351ed-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="351ed-154">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="351ed-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="351ed-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="351ed-155">RELATED LINKS</span></span>

