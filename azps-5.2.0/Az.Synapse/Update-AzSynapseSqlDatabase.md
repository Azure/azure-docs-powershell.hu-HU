---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330785"
---
# <span data-ttu-id="648e4-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="648e4-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="648e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="648e4-102">SYNOPSIS</span></span>
<span data-ttu-id="648e4-103">Frissíti a Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="648e4-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="648e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="648e4-104">SYNTAX</span></span>

### <span data-ttu-id="648e4-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="648e4-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="648e4-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="648e4-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="648e4-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="648e4-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="648e4-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="648e4-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="648e4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="648e4-109">DESCRIPTION</span></span>
<span data-ttu-id="648e4-110">Az **Update-AzSynapseSqlDatabase** parancsmag frissíti az Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="648e4-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="648e4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="648e4-111">EXAMPLES</span></span>

### <span data-ttu-id="648e4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="648e4-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="648e4-113">Ez a parancs frissíti az Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="648e4-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="648e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="648e4-114">PARAMETERS</span></span>

### <span data-ttu-id="648e4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="648e4-115">-AsJob</span></span>
<span data-ttu-id="648e4-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="648e4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="648e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="648e4-117">-DefaultProfile</span></span>
<span data-ttu-id="648e4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="648e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="648e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="648e4-119">-InputObject</span></span>
<span data-ttu-id="648e4-120">SQL-adatbázis bemeneti objektuma, amely általában a folyamaton keresztül van átfutva.</span><span class="sxs-lookup"><span data-stu-id="648e4-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="648e4-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="648e4-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="648e4-122">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="648e4-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="648e4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="648e4-123">-Name</span></span>
<span data-ttu-id="648e4-124">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="648e4-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="648e4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="648e4-125">-PassThru</span></span>
<span data-ttu-id="648e4-126">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="648e4-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="648e4-127">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="648e4-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="648e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="648e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="648e4-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="648e4-129">Resource group name.</span></span>

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

### <span data-ttu-id="648e4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="648e4-130">-ResourceId</span></span>
<span data-ttu-id="648e4-131">A Synapse SQL-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="648e4-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="648e4-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="648e4-132">-Tag</span></span>
<span data-ttu-id="648e4-133">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="648e4-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="648e4-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="648e4-134">-WorkspaceName</span></span>
<span data-ttu-id="648e4-135">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="648e4-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="648e4-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="648e4-136">-WorkspaceObject</span></span>
<span data-ttu-id="648e4-137">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="648e4-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="648e4-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="648e4-138">-Confirm</span></span>
<span data-ttu-id="648e4-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="648e4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="648e4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="648e4-140">-WhatIf</span></span>
<span data-ttu-id="648e4-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="648e4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="648e4-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="648e4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="648e4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="648e4-143">CommonParameters</span></span>
<span data-ttu-id="648e4-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="648e4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="648e4-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="648e4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="648e4-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="648e4-146">INPUTS</span></span>

### <span data-ttu-id="648e4-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="648e4-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="648e4-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="648e4-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="648e4-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="648e4-149">OUTPUTS</span></span>

### <span data-ttu-id="648e4-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="648e4-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="648e4-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="648e4-151">NOTES</span></span>

## <span data-ttu-id="648e4-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="648e4-152">RELATED LINKS</span></span>
