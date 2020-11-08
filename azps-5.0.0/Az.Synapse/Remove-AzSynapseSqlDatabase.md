---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187136"
---
# <span data-ttu-id="a1303-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a1303-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="a1303-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1303-102">SYNOPSIS</span></span>
<span data-ttu-id="a1303-103">Egy szinapszis-Analytics SQL-adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="a1303-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a1303-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1303-104">SYNTAX</span></span>

### <span data-ttu-id="a1303-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1303-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1303-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1303-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1303-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1303-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1303-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1303-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1303-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1303-109">DESCRIPTION</span></span>
<span data-ttu-id="a1303-110">A **Remove-AzSynapseSqlPool** parancsmag véglegesen törli az Azure SZINAPSZIS Analytics SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="a1303-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="a1303-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a1303-111">EXAMPLES</span></span>

### <span data-ttu-id="a1303-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1303-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="a1303-113">Ez a parancs törli az Azure szinapszis Analytics SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="a1303-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="a1303-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a1303-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="a1303-115">Ez a parancs egy Azure szinapszis-Analytics SQL-adatbázist csővezetéken keresztül töröl.</span><span class="sxs-lookup"><span data-stu-id="a1303-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="a1303-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a1303-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="a1303-117">Ez a parancs egy Azure szinapszis-Analytics SQL-adatbázist csővezetéken keresztül töröl.</span><span class="sxs-lookup"><span data-stu-id="a1303-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="a1303-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="a1303-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="a1303-119">Ez a parancs törli az Azure szinapszis-Analytics SQL-adatbázisát a megadott erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="a1303-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="a1303-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1303-120">PARAMETERS</span></span>

### <span data-ttu-id="a1303-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1303-121">-AsJob</span></span>
<span data-ttu-id="a1303-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a1303-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1303-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1303-123">-DefaultProfile</span></span>
<span data-ttu-id="a1303-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1303-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1303-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1303-125">-InputObject</span></span>
<span data-ttu-id="a1303-126">SQL-adatbázis bemeneti objektuma, általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a1303-126">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1303-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1303-127">-Name</span></span>
<span data-ttu-id="a1303-128">A szinapszis SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a1303-128">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="a1303-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1303-129">-PassThru</span></span>
<span data-ttu-id="a1303-130">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="a1303-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a1303-131">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="a1303-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a1303-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1303-132">-ResourceGroupName</span></span>
<span data-ttu-id="a1303-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a1303-133">Resource group name.</span></span>

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

### <span data-ttu-id="a1303-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1303-134">-ResourceId</span></span>
<span data-ttu-id="a1303-135">A szinapszis SQL-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1303-135">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="a1303-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1303-136">-WorkspaceName</span></span>
<span data-ttu-id="a1303-137">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="a1303-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a1303-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a1303-138">-WorkspaceObject</span></span>
<span data-ttu-id="a1303-139">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a1303-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1303-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1303-140">-Confirm</span></span>
<span data-ttu-id="a1303-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1303-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1303-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1303-142">-WhatIf</span></span>
<span data-ttu-id="a1303-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1303-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1303-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1303-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1303-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1303-145">CommonParameters</span></span>
<span data-ttu-id="a1303-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1303-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1303-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1303-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1303-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1303-148">INPUTS</span></span>

### <span data-ttu-id="a1303-149">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1303-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a1303-150">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a1303-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="a1303-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a1303-151">System.String</span></span>

## <span data-ttu-id="a1303-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1303-152">OUTPUTS</span></span>

### <span data-ttu-id="a1303-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1303-153">System.Boolean</span></span>

## <span data-ttu-id="a1303-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1303-154">NOTES</span></span>

## <span data-ttu-id="a1303-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1303-155">RELATED LINKS</span></span>
