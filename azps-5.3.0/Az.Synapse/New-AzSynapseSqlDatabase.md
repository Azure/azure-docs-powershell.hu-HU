---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383584"
---
# <span data-ttu-id="59d80-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59d80-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="59d80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d80-102">SYNOPSIS</span></span>
<span data-ttu-id="59d80-103">Synapse Analytics SQL-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="59d80-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="59d80-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59d80-104">SYNTAX</span></span>

### <span data-ttu-id="59d80-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59d80-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d80-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59d80-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d80-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59d80-107">DESCRIPTION</span></span>
<span data-ttu-id="59d80-108">A **Get-AzSynapseSqlDatabase** parancsmag információkat kap egy Azure Synapse Analytics SQL-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="59d80-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="59d80-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59d80-109">EXAMPLES</span></span>

### <span data-ttu-id="59d80-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="59d80-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="59d80-111">Ez a parancs létrehoz egy Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="59d80-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="59d80-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59d80-112">PARAMETERS</span></span>

### <span data-ttu-id="59d80-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59d80-113">-AsJob</span></span>
<span data-ttu-id="59d80-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="59d80-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59d80-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="59d80-115">-Collation</span></span>
<span data-ttu-id="59d80-116">A Szétválogatás határozza meg az adatokat rendezési és összehasonlítási szabályokat, és nem módosíthatók az SQL-készlet létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="59d80-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="59d80-117">Az alapértelmezett szétválogatás SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="59d80-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="59d80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d80-118">-DefaultProfile</span></span>
<span data-ttu-id="59d80-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59d80-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d80-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="59d80-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="59d80-121">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="59d80-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d80-122">-Name</span><span class="sxs-lookup"><span data-stu-id="59d80-122">-Name</span></span>
<span data-ttu-id="59d80-123">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="59d80-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="59d80-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d80-124">-ResourceGroupName</span></span>
<span data-ttu-id="59d80-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="59d80-125">Resource group name.</span></span>

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

### <span data-ttu-id="59d80-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="59d80-126">-Tag</span></span>
<span data-ttu-id="59d80-127">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="59d80-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="59d80-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59d80-128">-WorkspaceName</span></span>
<span data-ttu-id="59d80-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="59d80-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="59d80-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="59d80-130">-WorkspaceObject</span></span>
<span data-ttu-id="59d80-131">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="59d80-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="59d80-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59d80-132">-Confirm</span></span>
<span data-ttu-id="59d80-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="59d80-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d80-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d80-134">-WhatIf</span></span>
<span data-ttu-id="59d80-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="59d80-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d80-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59d80-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d80-137">CommonParameters</span></span>
<span data-ttu-id="59d80-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d80-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59d80-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d80-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59d80-140">INPUTS</span></span>

### <span data-ttu-id="59d80-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="59d80-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="59d80-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59d80-142">OUTPUTS</span></span>

### <span data-ttu-id="59d80-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59d80-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="59d80-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59d80-144">NOTES</span></span>

## <span data-ttu-id="59d80-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59d80-145">RELATED LINKS</span></span>
