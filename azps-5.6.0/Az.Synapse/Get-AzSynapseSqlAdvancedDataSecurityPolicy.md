---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 47800968fec9a12255bae01499618f9928416648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015717"
---
# <span data-ttu-id="892c8-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="892c8-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="892c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="892c8-102">SYNOPSIS</span></span>
<span data-ttu-id="892c8-103">A munkaterület speciális adatbiztonsági házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="892c8-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="892c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="892c8-104">SYNTAX</span></span>

### <span data-ttu-id="892c8-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="892c8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="892c8-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="892c8-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="892c8-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="892c8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="892c8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="892c8-108">DESCRIPTION</span></span>
<span data-ttu-id="892c8-109">A **Get-AzSynapseSqlAdvancedDataSecurityPolicy** parancsmag beolvassa egy munkaterület speciális adatbiztonsági házirendjét.</span><span class="sxs-lookup"><span data-stu-id="892c8-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="892c8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="892c8-110">EXAMPLES</span></span>

### <span data-ttu-id="892c8-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="892c8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="892c8-112">Ez a parancs a Speciális adatbiztonság parancsot kapja a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="892c8-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="892c8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="892c8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="892c8-114">Ez a parancs a Speciális adatbiztonság parancsot kapja a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="892c8-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="892c8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="892c8-115">PARAMETERS</span></span>

### <span data-ttu-id="892c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892c8-116">-DefaultProfile</span></span>
<span data-ttu-id="892c8-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="892c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="892c8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="892c8-118">-InputObject</span></span>
<span data-ttu-id="892c8-119">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="892c8-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="892c8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892c8-120">-ResourceGroupName</span></span>
<span data-ttu-id="892c8-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="892c8-121">Resource group name.</span></span>

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

### <span data-ttu-id="892c8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="892c8-122">-ResourceId</span></span>
<span data-ttu-id="892c8-123">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="892c8-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="892c8-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="892c8-124">-WorkspaceName</span></span>
<span data-ttu-id="892c8-125">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="892c8-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="892c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892c8-126">CommonParameters</span></span>
<span data-ttu-id="892c8-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892c8-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="892c8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892c8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="892c8-129">INPUTS</span></span>

### <span data-ttu-id="892c8-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="892c8-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="892c8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="892c8-131">OUTPUTS</span></span>

### <span data-ttu-id="892c8-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="892c8-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="892c8-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="892c8-133">NOTES</span></span>

## <span data-ttu-id="892c8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="892c8-134">RELATED LINKS</span></span>
