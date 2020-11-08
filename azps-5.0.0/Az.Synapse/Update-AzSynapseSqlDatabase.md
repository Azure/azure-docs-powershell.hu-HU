---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186159"
---
# <span data-ttu-id="d6025-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6025-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="d6025-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6025-102">SYNOPSIS</span></span>
<span data-ttu-id="d6025-103">A szinapszis Analytics SQL-adatbázis frissítése</span><span class="sxs-lookup"><span data-stu-id="d6025-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d6025-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6025-104">SYNTAX</span></span>

### <span data-ttu-id="d6025-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6025-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6025-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6025-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6025-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6025-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6025-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6025-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6025-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6025-109">DESCRIPTION</span></span>
<span data-ttu-id="d6025-110">Az **Update-AzSynapseSqlDatabase** parancsmag egy Azure szinapszis-Analytics SQL-adatbázist frissít.</span><span class="sxs-lookup"><span data-stu-id="d6025-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d6025-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d6025-111">EXAMPLES</span></span>

### <span data-ttu-id="d6025-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6025-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="d6025-113">Ez a parancs frissíti az Azure szinapszis Analytics SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="d6025-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d6025-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6025-114">PARAMETERS</span></span>

### <span data-ttu-id="d6025-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6025-115">-AsJob</span></span>
<span data-ttu-id="d6025-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d6025-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6025-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6025-117">-DefaultProfile</span></span>
<span data-ttu-id="d6025-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6025-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6025-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6025-119">-InputObject</span></span>
<span data-ttu-id="d6025-120">SQL-adatbázis bemeneti objektuma, általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="d6025-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d6025-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="d6025-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="d6025-122">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="d6025-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="d6025-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6025-123">-Name</span></span>
<span data-ttu-id="d6025-124">A szinapszis SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d6025-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="d6025-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6025-125">-PassThru</span></span>
<span data-ttu-id="d6025-126">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="d6025-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d6025-127">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="d6025-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d6025-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6025-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6025-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d6025-129">Resource group name.</span></span>

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

### <span data-ttu-id="d6025-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6025-130">-ResourceId</span></span>
<span data-ttu-id="d6025-131">A szinapszis SQL-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6025-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="d6025-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="d6025-132">-Tag</span></span>
<span data-ttu-id="d6025-133">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="d6025-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="d6025-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d6025-134">-WorkspaceName</span></span>
<span data-ttu-id="d6025-135">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="d6025-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d6025-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d6025-136">-WorkspaceObject</span></span>
<span data-ttu-id="d6025-137">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="d6025-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d6025-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6025-138">-Confirm</span></span>
<span data-ttu-id="d6025-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6025-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6025-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6025-140">-WhatIf</span></span>
<span data-ttu-id="d6025-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6025-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6025-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6025-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6025-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6025-143">CommonParameters</span></span>
<span data-ttu-id="d6025-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6025-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6025-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6025-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6025-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6025-146">INPUTS</span></span>

### <span data-ttu-id="d6025-147">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6025-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d6025-148">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6025-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="d6025-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6025-149">OUTPUTS</span></span>

### <span data-ttu-id="d6025-150">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6025-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="d6025-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6025-151">NOTES</span></span>

## <span data-ttu-id="d6025-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6025-152">RELATED LINKS</span></span>
