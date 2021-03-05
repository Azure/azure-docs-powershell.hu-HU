---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 46f59df272a62ca9cd6b517d3672436a01a75ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000150"
---
# <span data-ttu-id="aa962-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="aa962-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="aa962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa962-102">SYNOPSIS</span></span>
<span data-ttu-id="aa962-103">Egyetlen grafikonos lekérdezést az erőforrásneve alapján lekérdez.</span><span class="sxs-lookup"><span data-stu-id="aa962-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="aa962-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aa962-104">SYNTAX</span></span>

### <span data-ttu-id="aa962-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa962-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa962-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="aa962-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aa962-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa962-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa962-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aa962-108">DESCRIPTION</span></span>
<span data-ttu-id="aa962-109">Egyetlen grafikonos lekérdezést az erőforrásneve alapján lekérdez.</span><span class="sxs-lookup"><span data-stu-id="aa962-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="aa962-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aa962-110">EXAMPLES</span></span>

### <span data-ttu-id="aa962-111">1. példa: Az erőforráscsoport összes erőforrás-grafikon lekérdezésének be kérése</span><span class="sxs-lookup"><span data-stu-id="aa962-111">Example 1: Get all resource graph queries under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="aa962-112">Ez a parancs az összes erőforrás-grafikon lekérdezést egy erőforráscsoport alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa962-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="aa962-113">2. példa: Erőforrás-grafikon lekérdezésének lekérdezése név szerint</span><span class="sxs-lookup"><span data-stu-id="aa962-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="aa962-114">Ez a parancs név szerint kap egy erőforrás-grafikon lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="aa962-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="aa962-115">2. példa: Erőforrás-grafikon lekérdezése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="aa962-115">Example 2: Get a resource graph query by object</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="aa962-116">Ez a parancs objektumról erőforrás-grafikonra vonatkozó lekérdezést kap.</span><span class="sxs-lookup"><span data-stu-id="aa962-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="aa962-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa962-117">PARAMETERS</span></span>

### <span data-ttu-id="aa962-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa962-118">-DefaultProfile</span></span>
<span data-ttu-id="aa962-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa962-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa962-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa962-120">-InputObject</span></span>
<span data-ttu-id="aa962-121">Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="aa962-121">Identity Parameter</span></span>

<span data-ttu-id="aa962-122">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="aa962-122">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa962-123">-Name</span><span class="sxs-lookup"><span data-stu-id="aa962-123">-Name</span></span>
<span data-ttu-id="aa962-124">A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="aa962-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="aa962-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa962-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa962-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa962-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa962-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa962-127">-SubscriptionId</span></span>
<span data-ttu-id="aa962-128">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aa962-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="aa962-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa962-129">CommonParameters</span></span>
<span data-ttu-id="aa962-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa962-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa962-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa962-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa962-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa962-132">INPUTS</span></span>

### <span data-ttu-id="aa962-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="aa962-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="aa962-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa962-134">OUTPUTS</span></span>

### <span data-ttu-id="aa962-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="aa962-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="aa962-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aa962-136">NOTES</span></span>

<span data-ttu-id="aa962-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aa962-137">ALIASES</span></span>

<span data-ttu-id="aa962-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="aa962-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa962-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="aa962-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa962-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa962-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa962-141">INPUTOBJECT: <IResourceGraphIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="aa962-141">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa962-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="aa962-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa962-143">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa962-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="aa962-144">`[ResourceName <String>]`: A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="aa962-144">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="aa962-145">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aa962-145">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="aa962-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa962-146">RELATED LINKS</span></span>

