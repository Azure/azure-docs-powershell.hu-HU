---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 4951fbe707dbae8c1fdff34e828e468a2d3168bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383387"
---
# <span data-ttu-id="205fb-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="205fb-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="205fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205fb-102">SYNOPSIS</span></span>
<span data-ttu-id="205fb-103">Egy Synapse Analytics SQL-adatbázis törlése.</span><span class="sxs-lookup"><span data-stu-id="205fb-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="205fb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="205fb-104">SYNTAX</span></span>

### <span data-ttu-id="205fb-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="205fb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205fb-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="205fb-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205fb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="205fb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205fb-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="205fb-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205fb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="205fb-109">DESCRIPTION</span></span>
<span data-ttu-id="205fb-110">A **Remove-AzSynapseSqlPool** parancsmag véglegesen töröl egy Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="205fb-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="205fb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="205fb-111">EXAMPLES</span></span>

### <span data-ttu-id="205fb-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="205fb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="205fb-113">Ez a parancs töröl egy Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="205fb-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="205fb-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="205fb-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="205fb-115">Ez a parancs egy Azure Synapse Analytics SQL-adatbázist töröl folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="205fb-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="205fb-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="205fb-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="205fb-117">Ez a parancs egy Azure Synapse Analytics SQL-adatbázist töröl folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="205fb-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="205fb-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="205fb-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="205fb-119">Ez a parancs törli a megadott erőforrás-azonosítójú Azure Synapse Analytics SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="205fb-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="205fb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="205fb-120">PARAMETERS</span></span>

### <span data-ttu-id="205fb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="205fb-121">-AsJob</span></span>
<span data-ttu-id="205fb-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="205fb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="205fb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205fb-123">-DefaultProfile</span></span>
<span data-ttu-id="205fb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="205fb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205fb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="205fb-125">-Force</span></span>
<span data-ttu-id="205fb-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="205fb-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="205fb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="205fb-127">-InputObject</span></span>
<span data-ttu-id="205fb-128">SQL-adatbázis bemeneti objektuma, amely általában a folyamaton keresztül van átfutva.</span><span class="sxs-lookup"><span data-stu-id="205fb-128">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205fb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="205fb-129">-Name</span></span>
<span data-ttu-id="205fb-130">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="205fb-130">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205fb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="205fb-131">-PassThru</span></span>
<span data-ttu-id="205fb-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="205fb-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="205fb-133">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="205fb-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="205fb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205fb-134">-ResourceGroupName</span></span>
<span data-ttu-id="205fb-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="205fb-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205fb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="205fb-136">-ResourceId</span></span>
<span data-ttu-id="205fb-137">A Synapse SQL-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="205fb-137">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="205fb-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="205fb-138">-WorkspaceName</span></span>
<span data-ttu-id="205fb-139">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="205fb-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205fb-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="205fb-140">-WorkspaceObject</span></span>
<span data-ttu-id="205fb-141">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="205fb-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205fb-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="205fb-142">-Confirm</span></span>
<span data-ttu-id="205fb-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="205fb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205fb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205fb-144">-WhatIf</span></span>
<span data-ttu-id="205fb-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="205fb-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205fb-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="205fb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205fb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205fb-147">CommonParameters</span></span>
<span data-ttu-id="205fb-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205fb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205fb-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="205fb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205fb-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="205fb-150">INPUTS</span></span>

### <span data-ttu-id="205fb-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="205fb-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="205fb-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="205fb-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="205fb-153">System.String</span><span class="sxs-lookup"><span data-stu-id="205fb-153">System.String</span></span>

## <span data-ttu-id="205fb-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="205fb-154">OUTPUTS</span></span>

### <span data-ttu-id="205fb-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="205fb-155">System.Boolean</span></span>

## <span data-ttu-id="205fb-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="205fb-156">NOTES</span></span>

## <span data-ttu-id="205fb-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="205fb-157">RELATED LINKS</span></span>
