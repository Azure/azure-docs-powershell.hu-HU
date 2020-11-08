---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185067"
---
# <span data-ttu-id="a50a9-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="a50a9-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="a50a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a50a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a50a9-103">Megkapja az egyéni erőforrás-szolgáltatói jegyzékfájlt.</span><span class="sxs-lookup"><span data-stu-id="a50a9-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="a50a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a50a9-104">SYNTAX</span></span>

### <span data-ttu-id="a50a9-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a50a9-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a50a9-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a50a9-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a50a9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a50a9-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a50a9-108">Lista</span><span class="sxs-lookup"><span data-stu-id="a50a9-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a50a9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a50a9-109">DESCRIPTION</span></span>
<span data-ttu-id="a50a9-110">Megkapja az egyéni erőforrás-szolgáltatói jegyzékfájlt.</span><span class="sxs-lookup"><span data-stu-id="a50a9-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="a50a9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a50a9-111">EXAMPLES</span></span>

### <span data-ttu-id="a50a9-112">Példa 1: az előfizetésben szereplő összes egyéni szolgáltató listázása</span><span class="sxs-lookup"><span data-stu-id="a50a9-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="a50a9-113">Az előfizetésben szereplő összes egyéni szolgáltató felsorolása</span><span class="sxs-lookup"><span data-stu-id="a50a9-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="a50a9-114">2. példa: egyetlen egyéni szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="a50a9-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="a50a9-115">Egyetlen egyéni szolgáltató adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a50a9-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="a50a9-116">A Format-List használatával megjelenítheti az objektum adatait a képernyőn.</span><span class="sxs-lookup"><span data-stu-id="a50a9-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="a50a9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a50a9-117">PARAMETERS</span></span>

### <span data-ttu-id="a50a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a50a9-118">-DefaultProfile</span></span>
<span data-ttu-id="a50a9-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a50a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a50a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a50a9-120">-InputObject</span></span>
<span data-ttu-id="a50a9-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a50a9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a50a9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a50a9-122">-Name</span></span>
<span data-ttu-id="a50a9-123">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="a50a9-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="a50a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a50a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="a50a9-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a50a9-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a50a9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a50a9-126">-SubscriptionId</span></span>
<span data-ttu-id="a50a9-127">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a50a9-127">The Azure subscription ID.</span></span>
<span data-ttu-id="a50a9-128">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a50a9-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a50a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a50a9-129">CommonParameters</span></span>
<span data-ttu-id="a50a9-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a50a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a50a9-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a50a9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a50a9-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a50a9-132">INPUTS</span></span>

### <span data-ttu-id="a50a9-133">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="a50a9-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="a50a9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a50a9-134">OUTPUTS</span></span>

### <span data-ttu-id="a50a9-135">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. modellek. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="a50a9-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="a50a9-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a50a9-136">NOTES</span></span>

<span data-ttu-id="a50a9-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a50a9-137">ALIASES</span></span>

<span data-ttu-id="a50a9-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a50a9-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a50a9-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a50a9-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a50a9-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a50a9-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a50a9-141">INPUTOBJECT <ICustomProvidersIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a50a9-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a50a9-142">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="a50a9-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="a50a9-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a50a9-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a50a9-144">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a50a9-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a50a9-145">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="a50a9-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="a50a9-146">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="a50a9-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="a50a9-147">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a50a9-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a50a9-148">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a50a9-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a50a9-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a50a9-149">RELATED LINKS</span></span>
