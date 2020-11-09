---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297344"
---
# <span data-ttu-id="07ca9-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="07ca9-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="07ca9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="07ca9-103">A munkaterületet vNet bámulja.</span><span class="sxs-lookup"><span data-stu-id="07ca9-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="07ca9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07ca9-104">SYNTAX</span></span>

### <span data-ttu-id="07ca9-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07ca9-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="07ca9-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="07ca9-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="07ca9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="07ca9-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="07ca9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="07ca9-108">DESCRIPTION</span></span>
<span data-ttu-id="07ca9-109">A munkaterületet vNet bámulja.</span><span class="sxs-lookup"><span data-stu-id="07ca9-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="07ca9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="07ca9-110">EXAMPLES</span></span>

### <span data-ttu-id="07ca9-111">1. példa: az összes vnet kilistázása egy databricks alatt</span><span class="sxs-lookup"><span data-stu-id="07ca9-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="07ca9-112">Ez a parancs felsorolja az összes vnet a databricks csoportban.</span><span class="sxs-lookup"><span data-stu-id="07ca9-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="07ca9-113">2. példa: vnet való Ismerkedés</span><span class="sxs-lookup"><span data-stu-id="07ca9-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="07ca9-114">Ez a parancs vnet-alapú kinézetet kap.</span><span class="sxs-lookup"><span data-stu-id="07ca9-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="07ca9-115">3. példa: vnet kikérése objektum alapján</span><span class="sxs-lookup"><span data-stu-id="07ca9-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="07ca9-116">Ez a parancs az objektum vnet.</span><span class="sxs-lookup"><span data-stu-id="07ca9-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="07ca9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07ca9-117">PARAMETERS</span></span>

### <span data-ttu-id="07ca9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ca9-118">-DefaultProfile</span></span>
<span data-ttu-id="07ca9-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07ca9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ca9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07ca9-120">-InputObject</span></span>
<span data-ttu-id="07ca9-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07ca9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07ca9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07ca9-122">-Name</span></span>
<span data-ttu-id="07ca9-123">Annak a munkaterület-vNet a neve, amelyen a peering látható.</span><span class="sxs-lookup"><span data-stu-id="07ca9-123">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ca9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07ca9-124">-PassThru</span></span>
<span data-ttu-id="07ca9-125">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="07ca9-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ca9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ca9-126">-ResourceGroupName</span></span>
<span data-ttu-id="07ca9-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="07ca9-127">The name of the resource group.</span></span>
<span data-ttu-id="07ca9-128">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="07ca9-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="07ca9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07ca9-129">-SubscriptionId</span></span>
<span data-ttu-id="07ca9-130">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07ca9-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ca9-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07ca9-131">-WorkspaceName</span></span>
<span data-ttu-id="07ca9-132">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="07ca9-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="07ca9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ca9-133">CommonParameters</span></span>
<span data-ttu-id="07ca9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07ca9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ca9-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07ca9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ca9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07ca9-136">INPUTS</span></span>

### <span data-ttu-id="07ca9-137">Microsoft. Azure. PowerShell. parancsmagok. Databricks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="07ca9-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="07ca9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07ca9-138">OUTPUTS</span></span>

### <span data-ttu-id="07ca9-139">Microsoft. Azure. PowerShell. parancsmagok. Databricks. modellek. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="07ca9-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="07ca9-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07ca9-140">NOTES</span></span>

<span data-ttu-id="07ca9-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="07ca9-141">ALIASES</span></span>

<span data-ttu-id="07ca9-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="07ca9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07ca9-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="07ca9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07ca9-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="07ca9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07ca9-145">INPUTOBJECT <IDatabricksIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="07ca9-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07ca9-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="07ca9-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07ca9-147">`[PeeringName <String>]`: A munkaterület vNete.</span><span class="sxs-lookup"><span data-stu-id="07ca9-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="07ca9-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="07ca9-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="07ca9-149">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="07ca9-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="07ca9-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07ca9-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="07ca9-151">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="07ca9-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="07ca9-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07ca9-152">RELATED LINKS</span></span>

