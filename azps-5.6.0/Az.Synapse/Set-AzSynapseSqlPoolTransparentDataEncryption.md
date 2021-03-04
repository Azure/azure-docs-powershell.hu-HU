---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cdc72a2bb0e21873bd0fa2d82123afe8ed011378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939210"
---
# <span data-ttu-id="509f3-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="509f3-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="509f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="509f3-102">SYNOPSIS</span></span>
<span data-ttu-id="509f3-103">Módosítja egy SQL-készlet TDE tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="509f3-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="509f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="509f3-104">SYNTAX</span></span>

### <span data-ttu-id="509f3-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="509f3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509f3-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="509f3-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509f3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="509f3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509f3-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="509f3-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="509f3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="509f3-109">DESCRIPTION</span></span>
<span data-ttu-id="509f3-110">A **Set-AzSynapseSqlPoolTransparentDataEncryption** parancsmag módosítja egy Azure Synapse Analytics SQL-készlet TDE tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="509f3-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="509f3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="509f3-111">EXAMPLES</span></span>

### <span data-ttu-id="509f3-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="509f3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="509f3-113">Ez a parancs engedélyezi a TDE-t a ContosoSqlPool nevű SQL-készlethez a ContosoWorkspace nevű munkaterület alatt.</span><span class="sxs-lookup"><span data-stu-id="509f3-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="509f3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="509f3-114">PARAMETERS</span></span>

### <span data-ttu-id="509f3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="509f3-115">-AsJob</span></span>
<span data-ttu-id="509f3-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="509f3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="509f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="509f3-117">-DefaultProfile</span></span>
<span data-ttu-id="509f3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="509f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="509f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="509f3-119">-InputObject</span></span>
<span data-ttu-id="509f3-120">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="509f3-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="509f3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="509f3-121">-Name</span></span>
<span data-ttu-id="509f3-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="509f3-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="509f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="509f3-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="509f3-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509f3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="509f3-125">-ResourceId</span></span>
<span data-ttu-id="509f3-126">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="509f3-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509f3-127">-State</span><span class="sxs-lookup"><span data-stu-id="509f3-127">-State</span></span>
<span data-ttu-id="509f3-128">Az Azure Synapse Analytics sql pool transparent data encryption state.</span><span class="sxs-lookup"><span data-stu-id="509f3-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509f3-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="509f3-129">-WorkspaceName</span></span>
<span data-ttu-id="509f3-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="509f3-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509f3-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="509f3-131">-WorkspaceObject</span></span>
<span data-ttu-id="509f3-132">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="509f3-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="509f3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="509f3-133">-Confirm</span></span>
<span data-ttu-id="509f3-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="509f3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="509f3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="509f3-135">-WhatIf</span></span>
<span data-ttu-id="509f3-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="509f3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="509f3-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="509f3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="509f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509f3-138">CommonParameters</span></span>
<span data-ttu-id="509f3-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="509f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509f3-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="509f3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509f3-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="509f3-141">INPUTS</span></span>

### <span data-ttu-id="509f3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="509f3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="509f3-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="509f3-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="509f3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="509f3-144">OUTPUTS</span></span>

### <span data-ttu-id="509f3-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="509f3-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="509f3-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="509f3-146">NOTES</span></span>

## <span data-ttu-id="509f3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="509f3-147">RELATED LINKS</span></span>
