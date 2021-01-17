---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468594"
---
# <span data-ttu-id="6d5df-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="6d5df-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="6d5df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5df-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5df-103">Egyetlen grafikonos lekérdezést az erőforrásneve alapján lekérdez.</span><span class="sxs-lookup"><span data-stu-id="6d5df-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="6d5df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d5df-104">SYNTAX</span></span>

### <span data-ttu-id="6d5df-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d5df-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d5df-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="6d5df-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d5df-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5df-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d5df-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d5df-108">DESCRIPTION</span></span>
<span data-ttu-id="6d5df-109">Egyetlen grafikonos lekérdezést az erőforrásneve alapján lekérdez.</span><span class="sxs-lookup"><span data-stu-id="6d5df-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="6d5df-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d5df-110">EXAMPLES</span></span>

### <span data-ttu-id="6d5df-111">1. példa: Az összes erőforrás-grafikon lekérdezésének lekérdezhető egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="6d5df-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="6d5df-112">Ez a parancs az összes erőforrás-grafikon lekérdezést egy erőforráscsoport alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6d5df-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="6d5df-113">2. példa: Erőforrás-grafikon lekérdezésének lekérdezése név szerint</span><span class="sxs-lookup"><span data-stu-id="6d5df-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="6d5df-114">Ez a parancs név szerint kap egy erőforrás-grafikon lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="6d5df-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="6d5df-115">2. példa: Erőforrás-grafikon lekérdezése objecy szerint</span><span class="sxs-lookup"><span data-stu-id="6d5df-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="6d5df-116">Ez a parancs objektumról erőforrás-grafikonra vonatkozó lekérdezést kap.</span><span class="sxs-lookup"><span data-stu-id="6d5df-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="6d5df-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d5df-117">PARAMETERS</span></span>

### <span data-ttu-id="6d5df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5df-118">-DefaultProfile</span></span>
<span data-ttu-id="6d5df-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d5df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5df-120">-InputObject</span></span>
<span data-ttu-id="6d5df-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6d5df-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5df-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6d5df-122">-Name</span></span>
<span data-ttu-id="6d5df-123">A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6d5df-123">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="6d5df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5df-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d5df-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d5df-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d5df-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d5df-126">-SubscriptionId</span></span>
<span data-ttu-id="6d5df-127">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d5df-127">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="6d5df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5df-128">CommonParameters</span></span>
<span data-ttu-id="6d5df-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d5df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5df-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d5df-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5df-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d5df-131">INPUTS</span></span>

### <span data-ttu-id="6d5df-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5df-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="6d5df-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d5df-133">OUTPUTS</span></span>

### <span data-ttu-id="6d5df-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="6d5df-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="6d5df-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d5df-135">NOTES</span></span>

<span data-ttu-id="6d5df-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6d5df-136">ALIASES</span></span>

<span data-ttu-id="6d5df-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6d5df-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d5df-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6d5df-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d5df-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d5df-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d5df-140">INPUTOBJECT: <IResourceGraphIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6d5df-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d5df-141">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6d5df-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d5df-142">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d5df-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6d5df-143">`[ResourceName <String>]`: A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6d5df-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="6d5df-144">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d5df-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="6d5df-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d5df-145">RELATED LINKS</span></span>

