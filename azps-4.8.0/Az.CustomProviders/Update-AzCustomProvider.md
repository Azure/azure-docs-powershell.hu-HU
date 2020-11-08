---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025448"
---
# <span data-ttu-id="38429-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="38429-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="38429-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38429-102">SYNOPSIS</span></span>
<span data-ttu-id="38429-103">Frissít egy meglévő egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="38429-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="38429-104">A JAVÍTÁSon keresztül jelenleg csak a címkéket lehet frissíteni.</span><span class="sxs-lookup"><span data-stu-id="38429-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="38429-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38429-105">SYNTAX</span></span>

### <span data-ttu-id="38429-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38429-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="38429-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="38429-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38429-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38429-108">DESCRIPTION</span></span>
<span data-ttu-id="38429-109">Frissít egy meglévő egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="38429-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="38429-110">A JAVÍTÁSon keresztül jelenleg csak a címkéket lehet frissíteni.</span><span class="sxs-lookup"><span data-stu-id="38429-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="38429-111">Példák</span><span class="sxs-lookup"><span data-stu-id="38429-111">EXAMPLES</span></span>

### <span data-ttu-id="38429-112">1. példa: Címkék hozzáadása egyéni szolgáltatóhoz</span><span class="sxs-lookup"><span data-stu-id="38429-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="38429-113">Frissítheti egy egyéni szolgáltató címkéit.</span><span class="sxs-lookup"><span data-stu-id="38429-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="38429-114">2. példa: az egyéni szolgáltató frissítése a csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="38429-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="38429-115">Egyéni szolgáltató frissítése a csővezetékek segítségével</span><span class="sxs-lookup"><span data-stu-id="38429-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="38429-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38429-116">PARAMETERS</span></span>

### <span data-ttu-id="38429-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38429-117">-DefaultProfile</span></span>
<span data-ttu-id="38429-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38429-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38429-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38429-119">-InputObject</span></span>
<span data-ttu-id="38429-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="38429-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38429-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38429-121">-Name</span></span>
<span data-ttu-id="38429-122">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="38429-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="38429-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38429-123">-ResourceGroupName</span></span>
<span data-ttu-id="38429-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38429-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="38429-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38429-125">-SubscriptionId</span></span>
<span data-ttu-id="38429-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38429-126">The Azure subscription ID.</span></span>
<span data-ttu-id="38429-127">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="38429-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="38429-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="38429-128">-Tag</span></span>
<span data-ttu-id="38429-129">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="38429-129">Resource tags</span></span>

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

### <span data-ttu-id="38429-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38429-130">-Confirm</span></span>
<span data-ttu-id="38429-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38429-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38429-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38429-132">-WhatIf</span></span>
<span data-ttu-id="38429-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38429-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38429-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38429-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38429-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38429-135">CommonParameters</span></span>
<span data-ttu-id="38429-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38429-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38429-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="38429-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38429-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38429-138">INPUTS</span></span>

### <span data-ttu-id="38429-139">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="38429-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="38429-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38429-140">OUTPUTS</span></span>

### <span data-ttu-id="38429-141">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. modellek. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="38429-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="38429-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38429-142">NOTES</span></span>

<span data-ttu-id="38429-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="38429-143">ALIASES</span></span>

<span data-ttu-id="38429-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="38429-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38429-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="38429-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38429-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="38429-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38429-147">INPUTOBJECT <ICustomProvidersIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="38429-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38429-148">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="38429-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="38429-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="38429-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38429-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38429-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="38429-151">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="38429-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="38429-152">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="38429-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="38429-153">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38429-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="38429-154">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="38429-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="38429-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38429-155">RELATED LINKS</span></span>

