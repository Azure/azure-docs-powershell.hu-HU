---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184559"
---
# <span data-ttu-id="714fc-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="714fc-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="714fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="714fc-102">SYNOPSIS</span></span>
<span data-ttu-id="714fc-103">Törli a munkaterület vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="714fc-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="714fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="714fc-104">SYNTAX</span></span>

### <span data-ttu-id="714fc-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="714fc-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="714fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="714fc-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="714fc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="714fc-107">DESCRIPTION</span></span>
<span data-ttu-id="714fc-108">Törli a munkaterület vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="714fc-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="714fc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="714fc-109">EXAMPLES</span></span>

### <span data-ttu-id="714fc-110">Példa 1: a databricks vnetének eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="714fc-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="714fc-111">Ez a parancs eltávolítja a databricks név szerinti vnet.</span><span class="sxs-lookup"><span data-stu-id="714fc-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="714fc-112">2. példa: vnet databricks eltávolítása objektumból</span><span class="sxs-lookup"><span data-stu-id="714fc-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="714fc-113">Ez a parancs eltávolítja a databricks objektum szerinti vnet.</span><span class="sxs-lookup"><span data-stu-id="714fc-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="714fc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="714fc-114">PARAMETERS</span></span>

### <span data-ttu-id="714fc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="714fc-115">-AsJob</span></span>
<span data-ttu-id="714fc-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="714fc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="714fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714fc-117">-DefaultProfile</span></span>
<span data-ttu-id="714fc-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="714fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="714fc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="714fc-119">-InputObject</span></span>
<span data-ttu-id="714fc-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="714fc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="714fc-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="714fc-121">-Name</span></span>
<span data-ttu-id="714fc-122">Annak a munkaterület-vNet a neve, amelyen a peering látható.</span><span class="sxs-lookup"><span data-stu-id="714fc-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="714fc-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="714fc-123">-NoWait</span></span>
<span data-ttu-id="714fc-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="714fc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="714fc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="714fc-125">-PassThru</span></span>
<span data-ttu-id="714fc-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="714fc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="714fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="714fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="714fc-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="714fc-128">The name of the resource group.</span></span>
<span data-ttu-id="714fc-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="714fc-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="714fc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="714fc-130">-SubscriptionId</span></span>
<span data-ttu-id="714fc-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="714fc-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="714fc-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="714fc-132">-WorkspaceName</span></span>
<span data-ttu-id="714fc-133">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="714fc-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="714fc-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="714fc-134">-Confirm</span></span>
<span data-ttu-id="714fc-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="714fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="714fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="714fc-136">-WhatIf</span></span>
<span data-ttu-id="714fc-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="714fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="714fc-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="714fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="714fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714fc-139">CommonParameters</span></span>
<span data-ttu-id="714fc-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="714fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714fc-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="714fc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714fc-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="714fc-142">INPUTS</span></span>

### <span data-ttu-id="714fc-143">Microsoft. Azure. PowerShell. parancsmagok. Databricks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="714fc-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="714fc-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="714fc-144">OUTPUTS</span></span>

### <span data-ttu-id="714fc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="714fc-145">System.Boolean</span></span>

## <span data-ttu-id="714fc-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="714fc-146">NOTES</span></span>

<span data-ttu-id="714fc-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="714fc-147">ALIASES</span></span>

<span data-ttu-id="714fc-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="714fc-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="714fc-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="714fc-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="714fc-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="714fc-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="714fc-151">INPUTOBJECT <IDatabricksIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="714fc-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="714fc-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="714fc-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="714fc-153">`[PeeringName <String>]`: A munkaterület vNete.</span><span class="sxs-lookup"><span data-stu-id="714fc-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="714fc-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="714fc-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="714fc-155">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="714fc-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="714fc-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="714fc-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="714fc-157">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="714fc-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="714fc-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="714fc-158">RELATED LINKS</span></span>

