---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467214"
---
# <span data-ttu-id="9ccd0-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="9ccd0-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="9ccd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ccd0-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccd0-103">Hozzon létre egy új grafikonos lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-103">Create a new graph query.</span></span>

## <span data-ttu-id="9ccd0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ccd0-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ccd0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ccd0-105">DESCRIPTION</span></span>
<span data-ttu-id="9ccd0-106">Hozzon létre egy új grafikonos lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-106">Create a new graph query.</span></span>

## <span data-ttu-id="9ccd0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ccd0-107">EXAMPLES</span></span>

### <span data-ttu-id="9ccd0-108">1. példa: Erőforrás-grafikon lekérdezés létrehozása a lekérdezés paramétere alapján</span><span class="sxs-lookup"><span data-stu-id="9ccd0-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="9ccd0-109">Ez a parancs egy erőforrás-grafikon lekérdezést hoz létre a lekérdezés paramétere alapján.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="9ccd0-110">2. példa: Erőforrás-grafikon lekérdezés létrehozása a fájl paramétere alapján</span><span class="sxs-lookup"><span data-stu-id="9ccd0-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="9ccd0-111">Ez a parancs egy erőforrás-grafikon lekérdezést hoz létre a fájl paramétere alapján.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="9ccd0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ccd0-112">PARAMETERS</span></span>

### <span data-ttu-id="9ccd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccd0-113">-DefaultProfile</span></span>
<span data-ttu-id="9ccd0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ccd0-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9ccd0-115">-Description</span></span>
<span data-ttu-id="9ccd0-116">A grafikonos lekérdezés leírása.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="9ccd0-117">-File</span><span class="sxs-lookup"><span data-stu-id="9ccd0-117">-File</span></span>
<span data-ttu-id="9ccd0-118">A fájl tartalma át lesz adva a lekérdezés paraméterének.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="9ccd0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9ccd0-119">-Location</span></span>
<span data-ttu-id="9ccd0-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="9ccd0-120">The location of the resource</span></span>

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

### <span data-ttu-id="9ccd0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9ccd0-121">-Name</span></span>
<span data-ttu-id="9ccd0-122">A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-122">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ccd0-123">-Query</span><span class="sxs-lookup"><span data-stu-id="9ccd0-123">-Query</span></span>
<span data-ttu-id="9ccd0-124">KQL-lekérdezés, amely grafikon lesz.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="9ccd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ccd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="9ccd0-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ccd0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ccd0-127">-SubscriptionId</span></span>
<span data-ttu-id="9ccd0-128">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ccd0-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ccd0-129">-Tag</span></span>
<span data-ttu-id="9ccd0-130">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="9ccd0-130">Resource tags</span></span>

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

### <span data-ttu-id="9ccd0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ccd0-131">-Confirm</span></span>
<span data-ttu-id="9ccd0-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ccd0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ccd0-133">-WhatIf</span></span>
<span data-ttu-id="9ccd0-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ccd0-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ccd0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccd0-136">CommonParameters</span></span>
<span data-ttu-id="9ccd0-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ccd0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccd0-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ccd0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccd0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ccd0-139">INPUTS</span></span>

### <span data-ttu-id="9ccd0-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="9ccd0-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="9ccd0-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="9ccd0-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="9ccd0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ccd0-142">OUTPUTS</span></span>

### <span data-ttu-id="9ccd0-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="9ccd0-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="9ccd0-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ccd0-144">NOTES</span></span>

<span data-ttu-id="9ccd0-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9ccd0-145">ALIASES</span></span>

## <span data-ttu-id="9ccd0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ccd0-146">RELATED LINKS</span></span>

