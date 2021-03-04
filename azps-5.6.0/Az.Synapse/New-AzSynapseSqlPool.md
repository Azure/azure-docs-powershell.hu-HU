---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 829227e47c0c68ac8ebe44f1a365898baa6e123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938433"
---
# <span data-ttu-id="5551a-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5551a-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5551a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5551a-102">SYNOPSIS</span></span>
<span data-ttu-id="5551a-103">Létrehoz egy Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="5551a-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5551a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5551a-104">SYNTAX</span></span>

### <span data-ttu-id="5551a-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5551a-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5551a-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5551a-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5551a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5551a-107">DESCRIPTION</span></span>
<span data-ttu-id="5551a-108">A **New-AzSynapseSqlPool** parancsmag létrehoz egy Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="5551a-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5551a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5551a-109">EXAMPLES</span></span>

### <span data-ttu-id="5551a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5551a-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="5551a-111">Ez a parancs létrehoz egy Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="5551a-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5551a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5551a-112">PARAMETERS</span></span>

### <span data-ttu-id="5551a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5551a-113">-AsJob</span></span>
<span data-ttu-id="5551a-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5551a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5551a-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="5551a-115">-Collation</span></span>
<span data-ttu-id="5551a-116">A Szétválogatás definiálja azokat a szabályokat, amelyek rendezik és hasonlítják az adatokat, és nem módosíthatók az SQL-készlet létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="5551a-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="5551a-117">Az alapértelmezett szétválogatás SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="5551a-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="5551a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5551a-118">-DefaultProfile</span></span>
<span data-ttu-id="5551a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5551a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5551a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5551a-120">-Name</span></span>
<span data-ttu-id="5551a-121">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="5551a-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5551a-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="5551a-122">-PerformanceLevel</span></span>
<span data-ttu-id="5551a-123">Az SQL-készlethez hozzárendelni szükséges SQL-szolgáltatásréteg és teljesítményszint.</span><span class="sxs-lookup"><span data-stu-id="5551a-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="5551a-124">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="5551a-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="5551a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5551a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5551a-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5551a-126">Resource group name.</span></span>

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

### <span data-ttu-id="5551a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="5551a-127">-Tag</span></span>
<span data-ttu-id="5551a-128">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="5551a-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5551a-129">-Version</span><span class="sxs-lookup"><span data-stu-id="5551a-129">-Version</span></span>
<span data-ttu-id="5551a-130">A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="5551a-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="5551a-131">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="5551a-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="5551a-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5551a-132">-WorkspaceName</span></span>
<span data-ttu-id="5551a-133">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="5551a-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5551a-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5551a-134">-WorkspaceObject</span></span>
<span data-ttu-id="5551a-135">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="5551a-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5551a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5551a-136">-Confirm</span></span>
<span data-ttu-id="5551a-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5551a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5551a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5551a-138">-WhatIf</span></span>
<span data-ttu-id="5551a-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5551a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5551a-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5551a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5551a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5551a-141">CommonParameters</span></span>
<span data-ttu-id="5551a-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5551a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5551a-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5551a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5551a-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5551a-144">INPUTS</span></span>

### <span data-ttu-id="5551a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5551a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5551a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5551a-146">OUTPUTS</span></span>

### <span data-ttu-id="5551a-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5551a-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5551a-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5551a-148">NOTES</span></span>

## <span data-ttu-id="5551a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5551a-149">RELATED LINKS</span></span>
