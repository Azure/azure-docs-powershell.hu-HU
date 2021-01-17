---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476565"
---
# <span data-ttu-id="80bf5-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="80bf5-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="80bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="80bf5-103">Módosítja egy SQL-készlet TDE tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="80bf5-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="80bf5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80bf5-104">SYNTAX</span></span>

### <span data-ttu-id="80bf5-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80bf5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80bf5-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bf5-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80bf5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bf5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80bf5-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bf5-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80bf5-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80bf5-109">DESCRIPTION</span></span>
<span data-ttu-id="80bf5-110">A **Set-AzSynapseSqlPoolTransparentDataEncryption** parancsmag módosítja egy Azure Synapse Analytics SQL-készlet TDE tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="80bf5-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="80bf5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80bf5-111">EXAMPLES</span></span>

### <span data-ttu-id="80bf5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="80bf5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="80bf5-113">Ez a parancs engedélyezi a TDE-t a ContosoSqlPool nevű SQL-készlethez a ContosoWorkspace nevű munkaterület alatt.</span><span class="sxs-lookup"><span data-stu-id="80bf5-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="80bf5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80bf5-114">PARAMETERS</span></span>

### <span data-ttu-id="80bf5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80bf5-115">-AsJob</span></span>
<span data-ttu-id="80bf5-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="80bf5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80bf5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bf5-117">-DefaultProfile</span></span>
<span data-ttu-id="80bf5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80bf5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80bf5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80bf5-119">-InputObject</span></span>
<span data-ttu-id="80bf5-120">SQL-készlet bemeneti objektuma, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="80bf5-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="80bf5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="80bf5-121">-Name</span></span>
<span data-ttu-id="80bf5-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="80bf5-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="80bf5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80bf5-123">-ResourceGroupName</span></span>
<span data-ttu-id="80bf5-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80bf5-124">Resource group name.</span></span>

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

### <span data-ttu-id="80bf5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80bf5-125">-ResourceId</span></span>
<span data-ttu-id="80bf5-126">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="80bf5-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="80bf5-127">-State</span><span class="sxs-lookup"><span data-stu-id="80bf5-127">-State</span></span>
<span data-ttu-id="80bf5-128">Az Azure Synapse Analytics sql pool transparent data encryption state.</span><span class="sxs-lookup"><span data-stu-id="80bf5-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="80bf5-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="80bf5-129">-WorkspaceName</span></span>
<span data-ttu-id="80bf5-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="80bf5-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="80bf5-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="80bf5-131">-WorkspaceObject</span></span>
<span data-ttu-id="80bf5-132">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="80bf5-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="80bf5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80bf5-133">-Confirm</span></span>
<span data-ttu-id="80bf5-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="80bf5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80bf5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80bf5-135">-WhatIf</span></span>
<span data-ttu-id="80bf5-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="80bf5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80bf5-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80bf5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80bf5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bf5-138">CommonParameters</span></span>
<span data-ttu-id="80bf5-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80bf5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bf5-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80bf5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bf5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80bf5-141">INPUTS</span></span>

### <span data-ttu-id="80bf5-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="80bf5-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="80bf5-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="80bf5-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="80bf5-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80bf5-144">OUTPUTS</span></span>

### <span data-ttu-id="80bf5-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="80bf5-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="80bf5-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80bf5-146">NOTES</span></span>

## <span data-ttu-id="80bf5-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80bf5-147">RELATED LINKS</span></span>
