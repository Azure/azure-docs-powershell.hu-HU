---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149987"
---
# <span data-ttu-id="0fc49-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0fc49-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="0fc49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc49-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc49-103">Létrehozza a Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="0fc49-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0fc49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0fc49-104">SYNTAX</span></span>

### <span data-ttu-id="0fc49-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fc49-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc49-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fc49-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc49-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0fc49-107">DESCRIPTION</span></span>
<span data-ttu-id="0fc49-108">A **Get-AzSynapseSqlDatabase** parancsmag információkat kap egy Azure Synapse Analytics SQL-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="0fc49-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0fc49-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0fc49-109">EXAMPLES</span></span>

### <span data-ttu-id="0fc49-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="0fc49-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="0fc49-111">Ez a parancs létrehoz egy Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="0fc49-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0fc49-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fc49-112">PARAMETERS</span></span>

### <span data-ttu-id="0fc49-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fc49-113">-AsJob</span></span>
<span data-ttu-id="0fc49-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0fc49-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fc49-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="0fc49-115">-Collation</span></span>
<span data-ttu-id="0fc49-116">A Szétválogatás definiálja azokat a szabályokat, amelyek rendezik és hasonlítják az adatokat, és nem módosíthatók az SQL-készlet létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="0fc49-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="0fc49-117">Az alapértelmezett szétválogatás SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="0fc49-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="0fc49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc49-118">-DefaultProfile</span></span>
<span data-ttu-id="0fc49-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fc49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc49-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="0fc49-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="0fc49-121">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="0fc49-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="0fc49-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0fc49-122">-Name</span></span>
<span data-ttu-id="0fc49-123">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0fc49-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="0fc49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc49-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fc49-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fc49-125">Resource group name.</span></span>

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

### <span data-ttu-id="0fc49-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fc49-126">-Tag</span></span>
<span data-ttu-id="0fc49-127">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="0fc49-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="0fc49-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0fc49-128">-WorkspaceName</span></span>
<span data-ttu-id="0fc49-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="0fc49-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0fc49-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0fc49-130">-WorkspaceObject</span></span>
<span data-ttu-id="0fc49-131">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="0fc49-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0fc49-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fc49-132">-Confirm</span></span>
<span data-ttu-id="0fc49-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0fc49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc49-134">-WhatIf</span></span>
<span data-ttu-id="0fc49-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0fc49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc49-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fc49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc49-137">CommonParameters</span></span>
<span data-ttu-id="0fc49-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc49-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fc49-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc49-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fc49-140">INPUTS</span></span>

### <span data-ttu-id="0fc49-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0fc49-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0fc49-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fc49-142">OUTPUTS</span></span>

### <span data-ttu-id="0fc49-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0fc49-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="0fc49-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0fc49-144">NOTES</span></span>

## <span data-ttu-id="0fc49-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fc49-145">RELATED LINKS</span></span>
