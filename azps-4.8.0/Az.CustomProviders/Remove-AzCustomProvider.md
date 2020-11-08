---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185058"
---
# <span data-ttu-id="745cb-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="745cb-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="745cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="745cb-102">SYNOPSIS</span></span>
<span data-ttu-id="745cb-103">Törli az egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="745cb-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="745cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="745cb-104">SYNTAX</span></span>

### <span data-ttu-id="745cb-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="745cb-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="745cb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="745cb-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="745cb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="745cb-107">DESCRIPTION</span></span>
<span data-ttu-id="745cb-108">Törli az egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="745cb-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="745cb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="745cb-109">EXAMPLES</span></span>

### <span data-ttu-id="745cb-110">Példa 1: egyéni szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="745cb-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="745cb-111">Egyéni szolgáltató eltávolítása</span><span class="sxs-lookup"><span data-stu-id="745cb-111">Remove a custom provider</span></span>

### <span data-ttu-id="745cb-112">2. példa: egyéni szolgáltató eltávolítása a PassThru</span><span class="sxs-lookup"><span data-stu-id="745cb-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="745cb-113">Egyéni szolgáltató eltávolítása a PassThru funkció használatával a siker vagy a kudarc jelzésére.</span><span class="sxs-lookup"><span data-stu-id="745cb-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="745cb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="745cb-114">PARAMETERS</span></span>

### <span data-ttu-id="745cb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="745cb-115">-AsJob</span></span>
<span data-ttu-id="745cb-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="745cb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="745cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745cb-117">-DefaultProfile</span></span>
<span data-ttu-id="745cb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="745cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="745cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="745cb-119">-InputObject</span></span>
<span data-ttu-id="745cb-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="745cb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="745cb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="745cb-121">-Name</span></span>
<span data-ttu-id="745cb-122">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="745cb-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745cb-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="745cb-123">-NoWait</span></span>
<span data-ttu-id="745cb-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="745cb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="745cb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="745cb-125">-PassThru</span></span>
<span data-ttu-id="745cb-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="745cb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="745cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="745cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="745cb-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="745cb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="745cb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="745cb-129">-SubscriptionId</span></span>
<span data-ttu-id="745cb-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="745cb-130">The Azure subscription ID.</span></span>
<span data-ttu-id="745cb-131">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="745cb-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="745cb-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="745cb-132">-Confirm</span></span>
<span data-ttu-id="745cb-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="745cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="745cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="745cb-134">-WhatIf</span></span>
<span data-ttu-id="745cb-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="745cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="745cb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="745cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="745cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745cb-137">CommonParameters</span></span>
<span data-ttu-id="745cb-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="745cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745cb-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="745cb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745cb-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="745cb-140">INPUTS</span></span>

### <span data-ttu-id="745cb-141">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="745cb-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="745cb-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="745cb-142">OUTPUTS</span></span>

### <span data-ttu-id="745cb-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="745cb-143">System.Boolean</span></span>

## <span data-ttu-id="745cb-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="745cb-144">NOTES</span></span>

<span data-ttu-id="745cb-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="745cb-145">ALIASES</span></span>

<span data-ttu-id="745cb-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="745cb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="745cb-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="745cb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="745cb-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="745cb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="745cb-149">INPUTOBJECT <ICustomProvidersIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="745cb-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="745cb-150">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="745cb-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="745cb-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="745cb-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="745cb-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="745cb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="745cb-153">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="745cb-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="745cb-154">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="745cb-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="745cb-155">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="745cb-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="745cb-156">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="745cb-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="745cb-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="745cb-157">RELATED LINKS</span></span>

