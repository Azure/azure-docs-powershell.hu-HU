---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195004"
---
# <span data-ttu-id="07bd3-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="07bd3-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="07bd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="07bd3-103">A szinapszis Analytics SQL-készlet létrehozása.</span><span class="sxs-lookup"><span data-stu-id="07bd3-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="07bd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07bd3-104">SYNTAX</span></span>

### <span data-ttu-id="07bd3-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07bd3-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bd3-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07bd3-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07bd3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="07bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="07bd3-108">A **New-AzSynapseSqlPool** parancsmag az Azure SZINAPSZIS Analytics SQL poolját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="07bd3-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="07bd3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="07bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="07bd3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07bd3-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="07bd3-111">A parancs létrehoz egy Azure szinapszis-Analytics SQL-medencét.</span><span class="sxs-lookup"><span data-stu-id="07bd3-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="07bd3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07bd3-112">PARAMETERS</span></span>

### <span data-ttu-id="07bd3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07bd3-113">-AsJob</span></span>
<span data-ttu-id="07bd3-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="07bd3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07bd3-115">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="07bd3-115">-Collation</span></span>
<span data-ttu-id="07bd3-116">A szétválogatás az adatrendezési és-összehasonlító szabályokat határozza meg, az SQL-készlet létrehozása után azonban nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="07bd3-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="07bd3-117">Az alapértelmezett rendezési sorrend SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="07bd3-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="07bd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bd3-118">-DefaultProfile</span></span>
<span data-ttu-id="07bd3-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07bd3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07bd3-120">-Name</span></span>
<span data-ttu-id="07bd3-121">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="07bd3-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="07bd3-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="07bd3-122">-PerformanceLevel</span></span>
<span data-ttu-id="07bd3-123">Az SQL-szolgáltatási szint és a teljesítmény szint az SQL-készlethez való hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="07bd3-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="07bd3-124">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="07bd3-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="07bd3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bd3-125">-ResourceGroupName</span></span>
<span data-ttu-id="07bd3-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="07bd3-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd3-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="07bd3-127">-Tag</span></span>
<span data-ttu-id="07bd3-128">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="07bd3-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="07bd3-129">-Verzió</span><span class="sxs-lookup"><span data-stu-id="07bd3-129">-Version</span></span>
<span data-ttu-id="07bd3-130">A szinapszis SQL Pool verziója.</span><span class="sxs-lookup"><span data-stu-id="07bd3-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="07bd3-131">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="07bd3-131">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd3-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07bd3-132">-WorkspaceName</span></span>
<span data-ttu-id="07bd3-133">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="07bd3-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd3-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="07bd3-134">-WorkspaceObject</span></span>
<span data-ttu-id="07bd3-135">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="07bd3-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07bd3-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07bd3-136">-Confirm</span></span>
<span data-ttu-id="07bd3-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07bd3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07bd3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bd3-138">-WhatIf</span></span>
<span data-ttu-id="07bd3-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07bd3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07bd3-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07bd3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07bd3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bd3-141">CommonParameters</span></span>
<span data-ttu-id="07bd3-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07bd3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bd3-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07bd3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bd3-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07bd3-144">INPUTS</span></span>

### <span data-ttu-id="07bd3-145">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07bd3-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="07bd3-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07bd3-146">OUTPUTS</span></span>

### <span data-ttu-id="07bd3-147">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="07bd3-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="07bd3-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07bd3-148">NOTES</span></span>

## <span data-ttu-id="07bd3-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07bd3-149">RELATED LINKS</span></span>
