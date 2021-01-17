---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359420"
---
# <span data-ttu-id="e5736-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="e5736-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="e5736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5736-102">SYNOPSIS</span></span>
<span data-ttu-id="e5736-103">Az Azure Synapse Analytics Workspace naplózási beállításait használja.</span><span class="sxs-lookup"><span data-stu-id="e5736-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e5736-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5736-104">SYNTAX</span></span>

### <span data-ttu-id="e5736-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5736-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5736-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5736-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5736-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5736-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5736-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5736-108">DESCRIPTION</span></span>
<span data-ttu-id="e5736-109">A **Get-AzSynapseSqlAuditSetting** parancsmag az Azure Synapse Analytics Workspace naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e5736-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e5736-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5736-110">EXAMPLES</span></span>

### <span data-ttu-id="e5736-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e5736-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e5736-112">A ContosoWorkspace nevű munkaterület naplózási beállításait használja.</span><span class="sxs-lookup"><span data-stu-id="e5736-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e5736-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e5736-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="e5736-114">A ContosoWorkspace nevű munkaterület naplózási beállításait prognózison keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e5736-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e5736-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5736-115">PARAMETERS</span></span>

### <span data-ttu-id="e5736-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5736-116">-DefaultProfile</span></span>
<span data-ttu-id="e5736-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5736-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5736-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5736-118">-InputObject</span></span>
<span data-ttu-id="e5736-119">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5736-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5736-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5736-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5736-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e5736-121">Resource group name.</span></span>

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

### <span data-ttu-id="e5736-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5736-122">-ResourceId</span></span>
<span data-ttu-id="e5736-123">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e5736-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="e5736-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5736-124">-WorkspaceName</span></span>
<span data-ttu-id="e5736-125">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e5736-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e5736-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5736-126">CommonParameters</span></span>
<span data-ttu-id="e5736-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5736-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5736-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5736-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5736-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5736-129">INPUTS</span></span>

### <span data-ttu-id="e5736-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5736-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e5736-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5736-131">OUTPUTS</span></span>

### <span data-ttu-id="e5736-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="e5736-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="e5736-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5736-133">NOTES</span></span>

## <span data-ttu-id="e5736-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5736-134">RELATED LINKS</span></span>
