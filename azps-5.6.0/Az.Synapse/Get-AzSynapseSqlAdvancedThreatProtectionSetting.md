---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: f35e4787779c49b399659f5e01ed8002df2e19ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015702"
---
# <span data-ttu-id="605ef-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="605ef-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="605ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="605ef-102">SYNOPSIS</span></span>
<span data-ttu-id="605ef-103">A munkaterület komplex veszélyforrás-védelmi beállításainak megadása.</span><span class="sxs-lookup"><span data-stu-id="605ef-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="605ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="605ef-104">SYNTAX</span></span>

### <span data-ttu-id="605ef-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="605ef-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="605ef-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="605ef-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="605ef-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="605ef-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="605ef-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="605ef-108">DESCRIPTION</span></span>
<span data-ttu-id="605ef-109">A **Get-AzSynapseSqlAdvancedThreatProtectionSetting** parancsmag megkapja az Azure Synapse Analytics Workspace komplex veszélyforrás-védelmi beállításait.</span><span class="sxs-lookup"><span data-stu-id="605ef-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="605ef-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="605ef-110">EXAMPLES</span></span>

### <span data-ttu-id="605ef-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="605ef-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="605ef-112">Ez a parancs a ContosoWorkspace nevű munkaterület komplex veszélyforrás-védelmi beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="605ef-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="605ef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="605ef-113">PARAMETERS</span></span>

### <span data-ttu-id="605ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605ef-114">-DefaultProfile</span></span>
<span data-ttu-id="605ef-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="605ef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605ef-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="605ef-116">-InputObject</span></span>
<span data-ttu-id="605ef-117">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="605ef-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="605ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="605ef-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="605ef-119">Resource group name.</span></span>

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

### <span data-ttu-id="605ef-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="605ef-120">-ResourceId</span></span>
<span data-ttu-id="605ef-121">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="605ef-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="605ef-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="605ef-122">-WorkspaceName</span></span>
<span data-ttu-id="605ef-123">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="605ef-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="605ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605ef-124">CommonParameters</span></span>
<span data-ttu-id="605ef-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605ef-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="605ef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605ef-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="605ef-127">INPUTS</span></span>

### <span data-ttu-id="605ef-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="605ef-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="605ef-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="605ef-129">OUTPUTS</span></span>

### <span data-ttu-id="605ef-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="605ef-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="605ef-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="605ef-131">NOTES</span></span>

## <span data-ttu-id="605ef-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="605ef-132">RELATED LINKS</span></span>
