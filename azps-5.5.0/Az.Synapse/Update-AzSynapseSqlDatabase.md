---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149882"
---
# <span data-ttu-id="393f9-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="393f9-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="393f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="393f9-102">SYNOPSIS</span></span>
<span data-ttu-id="393f9-103">Frissíti a Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="393f9-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="393f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="393f9-104">SYNTAX</span></span>

### <span data-ttu-id="393f9-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="393f9-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="393f9-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="393f9-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="393f9-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="393f9-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="393f9-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="393f9-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="393f9-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="393f9-109">DESCRIPTION</span></span>
<span data-ttu-id="393f9-110">Az **Update-AzSynapseSqlDatabase** parancsmag frissíti az Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="393f9-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="393f9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="393f9-111">EXAMPLES</span></span>

### <span data-ttu-id="393f9-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="393f9-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="393f9-113">Ez a parancs frissíti az Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="393f9-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="393f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="393f9-114">PARAMETERS</span></span>

### <span data-ttu-id="393f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="393f9-115">-AsJob</span></span>
<span data-ttu-id="393f9-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="393f9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="393f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393f9-117">-DefaultProfile</span></span>
<span data-ttu-id="393f9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="393f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="393f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="393f9-119">-InputObject</span></span>
<span data-ttu-id="393f9-120">SQL-adatbázis bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="393f9-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="393f9-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="393f9-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="393f9-122">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="393f9-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393f9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="393f9-123">-Name</span></span>
<span data-ttu-id="393f9-124">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="393f9-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="393f9-125">-PassThru</span></span>
<span data-ttu-id="393f9-126">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="393f9-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="393f9-127">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="393f9-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="393f9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393f9-128">-ResourceGroupName</span></span>
<span data-ttu-id="393f9-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="393f9-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393f9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="393f9-130">-ResourceId</span></span>
<span data-ttu-id="393f9-131">A Synapse SQL-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="393f9-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393f9-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="393f9-132">-Tag</span></span>
<span data-ttu-id="393f9-133">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="393f9-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="393f9-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="393f9-134">-WorkspaceName</span></span>
<span data-ttu-id="393f9-135">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="393f9-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393f9-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="393f9-136">-WorkspaceObject</span></span>
<span data-ttu-id="393f9-137">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="393f9-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="393f9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="393f9-138">-Confirm</span></span>
<span data-ttu-id="393f9-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="393f9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="393f9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="393f9-140">-WhatIf</span></span>
<span data-ttu-id="393f9-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="393f9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="393f9-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="393f9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="393f9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393f9-143">CommonParameters</span></span>
<span data-ttu-id="393f9-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393f9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393f9-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="393f9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393f9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="393f9-146">INPUTS</span></span>

### <span data-ttu-id="393f9-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="393f9-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="393f9-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="393f9-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="393f9-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="393f9-149">OUTPUTS</span></span>

### <span data-ttu-id="393f9-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="393f9-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="393f9-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="393f9-151">NOTES</span></span>

## <span data-ttu-id="393f9-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="393f9-152">RELATED LINKS</span></span>
