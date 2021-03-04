---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 287472f89e7875411e287fa1315d5622a4c48a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942690"
---
# <span data-ttu-id="6cc41-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="6cc41-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="6cc41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc41-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc41-103">Az egyéni erőforrás-szolgáltató jegyzékfájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc41-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="6cc41-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cc41-104">SYNTAX</span></span>

### <span data-ttu-id="6cc41-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cc41-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6cc41-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="6cc41-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6cc41-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cc41-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6cc41-108">Lista</span><span class="sxs-lookup"><span data-stu-id="6cc41-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cc41-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cc41-109">DESCRIPTION</span></span>
<span data-ttu-id="6cc41-110">Az egyéni erőforrás-szolgáltató jegyzékfájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc41-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="6cc41-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cc41-111">EXAMPLES</span></span>

### <span data-ttu-id="6cc41-112">1. példa: Az előfizetés összes egyéni szolgáltatóának felsorolása</span><span class="sxs-lookup"><span data-stu-id="6cc41-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="6cc41-113">Az előfizetés összes egyéni szolgáltatója</span><span class="sxs-lookup"><span data-stu-id="6cc41-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="6cc41-114">2. példa: Egyetlen egyéni szolgáltató lekérte</span><span class="sxs-lookup"><span data-stu-id="6cc41-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

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

<span data-ttu-id="6cc41-115">Egyetlen egyéni szolgáltató adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc41-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="6cc41-116">Az Format-List objektum részleteinek a képernyőn való megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="6cc41-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="6cc41-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cc41-117">PARAMETERS</span></span>

### <span data-ttu-id="6cc41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc41-118">-DefaultProfile</span></span>
<span data-ttu-id="6cc41-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cc41-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc41-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cc41-120">-InputObject</span></span>
<span data-ttu-id="6cc41-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6cc41-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc41-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6cc41-122">-Name</span></span>
<span data-ttu-id="6cc41-123">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="6cc41-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc41-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc41-124">-ResourceGroupName</span></span>
<span data-ttu-id="6cc41-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cc41-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc41-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cc41-126">-SubscriptionId</span></span>
<span data-ttu-id="6cc41-127">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cc41-127">The Azure subscription ID.</span></span>
<span data-ttu-id="6cc41-128">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="6cc41-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6cc41-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc41-129">CommonParameters</span></span>
<span data-ttu-id="6cc41-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc41-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc41-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cc41-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc41-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cc41-132">INPUTS</span></span>

### <span data-ttu-id="6cc41-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="6cc41-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="6cc41-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc41-134">OUTPUTS</span></span>

### <span data-ttu-id="6cc41-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="6cc41-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="6cc41-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cc41-136">NOTES</span></span>

<span data-ttu-id="6cc41-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6cc41-137">ALIASES</span></span>

<span data-ttu-id="6cc41-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6cc41-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cc41-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6cc41-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cc41-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cc41-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cc41-141">INPUTOBJECT: <ICustomProvidersIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6cc41-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cc41-142">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="6cc41-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="6cc41-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6cc41-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cc41-144">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cc41-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6cc41-145">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="6cc41-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="6cc41-146">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="6cc41-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="6cc41-147">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cc41-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6cc41-148">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="6cc41-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6cc41-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cc41-149">RELATED LINKS</span></span>

