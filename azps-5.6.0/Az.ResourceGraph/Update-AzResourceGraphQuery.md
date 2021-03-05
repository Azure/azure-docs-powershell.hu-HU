---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 60dcb163e480371fe211651cc929b6335877490b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000101"
---
# <span data-ttu-id="36226-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="36226-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="36226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36226-102">SYNOPSIS</span></span>
<span data-ttu-id="36226-103">Egy már hozzáadott grafikonlekérdezés frissítése.</span><span class="sxs-lookup"><span data-stu-id="36226-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="36226-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36226-104">SYNTAX</span></span>

### <span data-ttu-id="36226-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36226-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36226-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36226-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36226-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36226-107">DESCRIPTION</span></span>
<span data-ttu-id="36226-108">Egy már hozzáadott grafikonlekérdezés frissítése.</span><span class="sxs-lookup"><span data-stu-id="36226-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="36226-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36226-109">EXAMPLES</span></span>

### <span data-ttu-id="36226-110">1. példa: A paraméteres lekérdezés frissítése és címke név szerint</span><span class="sxs-lookup"><span data-stu-id="36226-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="36226-111">Ez a parancs frissíti a paraméteres lekérdezést, és név szerint címkéz.</span><span class="sxs-lookup"><span data-stu-id="36226-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="36226-112">2. példa: A paraméterfájl frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="36226-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="36226-113">Ez a parancs frissíti a paraméteres lekérdezést, és objektum szerint címkéz.</span><span class="sxs-lookup"><span data-stu-id="36226-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="36226-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36226-114">PARAMETERS</span></span>

### <span data-ttu-id="36226-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36226-115">-DefaultProfile</span></span>
<span data-ttu-id="36226-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36226-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36226-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="36226-117">-Description</span></span>
<span data-ttu-id="36226-118">A grafikonos lekérdezés leírása.</span><span class="sxs-lookup"><span data-stu-id="36226-118">The description of a graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36226-119">-File</span><span class="sxs-lookup"><span data-stu-id="36226-119">-File</span></span>
<span data-ttu-id="36226-120">A fájl tartalma át lesz adva a lekérdezés paraméterének.</span><span class="sxs-lookup"><span data-stu-id="36226-120">The content of the file will be passed to the query parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36226-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36226-121">-InputObject</span></span>
<span data-ttu-id="36226-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="36226-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36226-123">-Name</span><span class="sxs-lookup"><span data-stu-id="36226-123">-Name</span></span>
<span data-ttu-id="36226-124">A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="36226-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="36226-125">-Query</span><span class="sxs-lookup"><span data-stu-id="36226-125">-Query</span></span>
<span data-ttu-id="36226-126">KQL-lekérdezés, amely grafikon lesz.</span><span class="sxs-lookup"><span data-stu-id="36226-126">KQL query that will be graph.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36226-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36226-127">-ResourceGroupName</span></span>
<span data-ttu-id="36226-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="36226-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="36226-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36226-129">-SubscriptionId</span></span>
<span data-ttu-id="36226-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="36226-130">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="36226-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="36226-131">-Tag</span></span>
<span data-ttu-id="36226-132">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="36226-132">Resource tags</span></span>

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

### <span data-ttu-id="36226-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36226-133">-Confirm</span></span>
<span data-ttu-id="36226-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36226-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36226-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36226-135">-WhatIf</span></span>
<span data-ttu-id="36226-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36226-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36226-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36226-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36226-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36226-138">CommonParameters</span></span>
<span data-ttu-id="36226-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36226-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36226-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36226-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36226-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36226-141">INPUTS</span></span>

### <span data-ttu-id="36226-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="36226-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="36226-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36226-143">OUTPUTS</span></span>

### <span data-ttu-id="36226-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="36226-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="36226-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36226-145">NOTES</span></span>

<span data-ttu-id="36226-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="36226-146">ALIASES</span></span>

<span data-ttu-id="36226-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="36226-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36226-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="36226-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36226-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36226-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36226-150">INPUTOBJECT: <IResourceGraphIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="36226-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36226-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="36226-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36226-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="36226-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="36226-153">`[ResourceName <String>]`: A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="36226-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="36226-154">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="36226-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="36226-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36226-155">RELATED LINKS</span></span>

