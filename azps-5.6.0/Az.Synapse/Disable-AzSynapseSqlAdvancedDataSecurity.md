---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 58b2aa2f62de5cc47a9319c9cf36b0d2c8d55975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923185"
---
# <span data-ttu-id="e0b24-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="e0b24-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="e0b24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b24-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b24-103">Letiltja a speciális adatbiztonságot a munkaterületeken.</span><span class="sxs-lookup"><span data-stu-id="e0b24-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="e0b24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0b24-104">SYNTAX</span></span>

### <span data-ttu-id="e0b24-105">DisableByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0b24-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b24-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b24-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b24-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b24-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b24-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0b24-108">DESCRIPTION</span></span>
<span data-ttu-id="e0b24-109">A **Disable-AzSynapseSqlAdvancedDataSecurity** parancsmag letiltja a speciális adatbiztonságot a munkaterületeken.</span><span class="sxs-lookup"><span data-stu-id="e0b24-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="e0b24-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0b24-110">EXAMPLES</span></span>

### <span data-ttu-id="e0b24-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0b24-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e0b24-112">Ez a parancs letiltja a Speciális adatbiztonságot a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="e0b24-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e0b24-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0b24-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="e0b24-114">Ez a parancs letiltja a Speciális adatbiztonságot a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="e0b24-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e0b24-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0b24-115">PARAMETERS</span></span>

### <span data-ttu-id="e0b24-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0b24-116">-AsJob</span></span>
<span data-ttu-id="e0b24-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e0b24-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0b24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b24-118">-DefaultProfile</span></span>
<span data-ttu-id="e0b24-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0b24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b24-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b24-120">-InputObject</span></span>
<span data-ttu-id="e0b24-121">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0b24-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b24-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b24-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0b24-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0b24-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b24-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0b24-124">-ResourceId</span></span>
<span data-ttu-id="e0b24-125">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0b24-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b24-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0b24-126">-WorkspaceName</span></span>
<span data-ttu-id="e0b24-127">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e0b24-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b24-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0b24-128">-Confirm</span></span>
<span data-ttu-id="e0b24-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e0b24-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b24-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b24-130">-WhatIf</span></span>
<span data-ttu-id="e0b24-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e0b24-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b24-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0b24-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b24-133">CommonParameters</span></span>
<span data-ttu-id="e0b24-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b24-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0b24-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b24-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0b24-136">INPUTS</span></span>

### <span data-ttu-id="e0b24-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0b24-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e0b24-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b24-138">OUTPUTS</span></span>

### <span data-ttu-id="e0b24-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="e0b24-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="e0b24-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0b24-140">NOTES</span></span>

## <span data-ttu-id="e0b24-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0b24-141">RELATED LINKS</span></span>
