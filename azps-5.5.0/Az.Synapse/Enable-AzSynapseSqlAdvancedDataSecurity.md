---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164635"
---
# <span data-ttu-id="9d802-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="9d802-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="9d802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d802-102">SYNOPSIS</span></span>
<span data-ttu-id="9d802-103">Speciális adatbiztonságot tesz lehetővé a munkaterületeken.</span><span class="sxs-lookup"><span data-stu-id="9d802-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="9d802-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d802-104">SYNTAX</span></span>

### <span data-ttu-id="9d802-105">EnableByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d802-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d802-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d802-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d802-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d802-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d802-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d802-108">DESCRIPTION</span></span>
<span data-ttu-id="9d802-109">Az **Enable-AzSynapseSqlAdvancedDataSecurity** parancsmag lehetővé teszi a speciális adatbiztonságot a munkaterületeken.</span><span class="sxs-lookup"><span data-stu-id="9d802-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="9d802-110">A Speciális adatbiztonság egy egységes biztonsági csomag, amely tartalmazza az adatbesorolást, a biztonsági rés felmérését és a komplex veszélyforrások elleni védelmet a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="9d802-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="9d802-111">(Automatikusan létrejön egy új tárfiók a biztonsági rések felmérésére.</span><span class="sxs-lookup"><span data-stu-id="9d802-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="9d802-112">Ha korábban erre a célra hoztak létre tárfiókot, azt használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="9d802-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="9d802-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d802-113">EXAMPLES</span></span>

### <span data-ttu-id="9d802-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="9d802-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9d802-115">Ez a parancs engedélyezi a munkaterület speciális adatbiztonságát.</span><span class="sxs-lookup"><span data-stu-id="9d802-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="9d802-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="9d802-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="9d802-117">Ez a parancs engedélyezi a munkaterület speciális adatbiztonságát a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="9d802-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="9d802-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="9d802-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="9d802-119">Ez a parancs engedélyezi a munkaterület speciális adatbiztonságát folyamaton keresztül, és nem teszi lehetővé automatikusan a biztonsági rés felmérését.</span><span class="sxs-lookup"><span data-stu-id="9d802-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="9d802-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d802-120">PARAMETERS</span></span>

### <span data-ttu-id="9d802-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d802-121">-AsJob</span></span>
<span data-ttu-id="9d802-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9d802-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d802-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d802-123">-DefaultProfile</span></span>
<span data-ttu-id="9d802-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d802-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d802-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9d802-125">-DeploymentName</span></span>
<span data-ttu-id="9d802-126">Egyéni nevet ad meg a speciális adatbiztonság-telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="9d802-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="9d802-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="9d802-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="9d802-128">Ne engedélyezze automatikusan a biztonsági rés felmérését (ezzel nem hoz létre tárfiókot).</span><span class="sxs-lookup"><span data-stu-id="9d802-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="9d802-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d802-129">-InputObject</span></span>
<span data-ttu-id="9d802-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="9d802-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d802-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d802-131">-ResourceGroupName</span></span>
<span data-ttu-id="9d802-132">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d802-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d802-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d802-133">-ResourceId</span></span>
<span data-ttu-id="9d802-134">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9d802-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d802-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d802-135">-WorkspaceName</span></span>
<span data-ttu-id="9d802-136">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9d802-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d802-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d802-137">-Confirm</span></span>
<span data-ttu-id="9d802-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9d802-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d802-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d802-139">-WhatIf</span></span>
<span data-ttu-id="9d802-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9d802-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d802-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d802-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d802-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d802-142">CommonParameters</span></span>
<span data-ttu-id="9d802-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d802-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d802-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d802-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d802-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d802-145">INPUTS</span></span>

### <span data-ttu-id="9d802-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d802-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9d802-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d802-147">OUTPUTS</span></span>

### <span data-ttu-id="9d802-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="9d802-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="9d802-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d802-149">NOTES</span></span>

## <span data-ttu-id="9d802-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d802-150">RELATED LINKS</span></span>
