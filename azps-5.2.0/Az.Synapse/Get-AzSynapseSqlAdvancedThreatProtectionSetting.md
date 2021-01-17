---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359434"
---
# <span data-ttu-id="cce29-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cce29-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cce29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce29-102">SYNOPSIS</span></span>
<span data-ttu-id="cce29-103">A munkaterület komplex veszélyforrások elleni védelmi beállításainak megadása.</span><span class="sxs-lookup"><span data-stu-id="cce29-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="cce29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cce29-104">SYNTAX</span></span>

### <span data-ttu-id="cce29-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cce29-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cce29-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cce29-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cce29-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cce29-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cce29-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cce29-108">DESCRIPTION</span></span>
<span data-ttu-id="cce29-109">A **Get-AzSynapseSqlAdvancedThreatProtectionSetting** parancsmag megkapja az Azure Synapse Analytics Workspace komplex veszélyforrás-védelmi beállításait.</span><span class="sxs-lookup"><span data-stu-id="cce29-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cce29-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cce29-110">EXAMPLES</span></span>

### <span data-ttu-id="cce29-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cce29-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cce29-112">Ez a parancs a ContosoWorkspace nevű munkaterület komplex veszélyforrás-védelmi beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cce29-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="cce29-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cce29-113">PARAMETERS</span></span>

### <span data-ttu-id="cce29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce29-114">-DefaultProfile</span></span>
<span data-ttu-id="cce29-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cce29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cce29-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cce29-116">-InputObject</span></span>
<span data-ttu-id="cce29-117">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="cce29-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cce29-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce29-118">-ResourceGroupName</span></span>
<span data-ttu-id="cce29-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cce29-119">Resource group name.</span></span>

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

### <span data-ttu-id="cce29-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cce29-120">-ResourceId</span></span>
<span data-ttu-id="cce29-121">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cce29-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cce29-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cce29-122">-WorkspaceName</span></span>
<span data-ttu-id="cce29-123">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="cce29-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cce29-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce29-124">CommonParameters</span></span>
<span data-ttu-id="cce29-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce29-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce29-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cce29-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce29-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cce29-127">INPUTS</span></span>

### <span data-ttu-id="cce29-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cce29-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cce29-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cce29-129">OUTPUTS</span></span>

### <span data-ttu-id="cce29-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="cce29-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="cce29-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cce29-131">NOTES</span></span>

## <span data-ttu-id="cce29-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cce29-132">RELATED LINKS</span></span>
