---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4e3b6b596f276f3d36a315354a93950524722adc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209039"
---
# <span data-ttu-id="2070c-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="2070c-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="2070c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2070c-102">SYNOPSIS</span></span>
<span data-ttu-id="2070c-103">Az SQL-készlet komplex veszélyforrások elleni védelemre vonatkozó speciális beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2070c-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="2070c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2070c-104">SYNTAX</span></span>

### <span data-ttu-id="2070c-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2070c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2070c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2070c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2070c-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2070c-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2070c-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2070c-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2070c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2070c-109">DESCRIPTION</span></span>
<span data-ttu-id="2070c-110">A **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** parancsmag megkapja az Azure Synapse Analytics SQL-készlet komplex veszélyforrás-védelmi beállításait.</span><span class="sxs-lookup"><span data-stu-id="2070c-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2070c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2070c-111">EXAMPLES</span></span>

### <span data-ttu-id="2070c-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2070c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2070c-113">Ez a parancs a ContosoSqlPool nevű SQL-készlet komplex veszélyforrás-védelmi beállításait kapja a ContosoWorkspace nevű munkaterület alatt.</span><span class="sxs-lookup"><span data-stu-id="2070c-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2070c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2070c-114">PARAMETERS</span></span>

### <span data-ttu-id="2070c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2070c-115">-DefaultProfile</span></span>
<span data-ttu-id="2070c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2070c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2070c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2070c-117">-InputObject</span></span>
<span data-ttu-id="2070c-118">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="2070c-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2070c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2070c-119">-Name</span></span>
<span data-ttu-id="2070c-120">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="2070c-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2070c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2070c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2070c-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2070c-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2070c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2070c-123">-ResourceId</span></span>
<span data-ttu-id="2070c-124">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2070c-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2070c-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2070c-125">-WorkspaceName</span></span>
<span data-ttu-id="2070c-126">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="2070c-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2070c-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2070c-127">-WorkspaceObject</span></span>
<span data-ttu-id="2070c-128">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="2070c-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2070c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2070c-129">CommonParameters</span></span>
<span data-ttu-id="2070c-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2070c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2070c-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2070c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2070c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2070c-132">INPUTS</span></span>

### <span data-ttu-id="2070c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2070c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2070c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2070c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2070c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2070c-135">OUTPUTS</span></span>

### <span data-ttu-id="2070c-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="2070c-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="2070c-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2070c-137">NOTES</span></span>

## <span data-ttu-id="2070c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2070c-138">RELATED LINKS</span></span>
