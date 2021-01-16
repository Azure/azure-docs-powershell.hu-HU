---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384074"
---
# <span data-ttu-id="6be48-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6be48-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="6be48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6be48-102">SYNOPSIS</span></span>
<span data-ttu-id="6be48-103">Leküldi az önkiszolgáló integrációs futásidejű billentyűparancsokat.</span><span class="sxs-lookup"><span data-stu-id="6be48-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="6be48-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6be48-104">SYNTAX</span></span>

### <span data-ttu-id="6be48-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6be48-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6be48-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6be48-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6be48-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6be48-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6be48-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6be48-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6be48-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6be48-109">DESCRIPTION</span></span>
<span data-ttu-id="6be48-110">A **Get-AzSynapseIntegrationRuntimeKey** parancsmag az integrációs futásidő kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6be48-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="6be48-111">A kulcsok egy integrációs futásidejű csomópont regisztrálását használják.</span><span class="sxs-lookup"><span data-stu-id="6be48-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="6be48-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6be48-112">EXAMPLES</span></span>

### <span data-ttu-id="6be48-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="6be48-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="6be48-114">A parancsmag lekéri a "test-selfhost-ir" nevű integrációs futási idő kulcsait.</span><span class="sxs-lookup"><span data-stu-id="6be48-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6be48-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6be48-115">PARAMETERS</span></span>

### <span data-ttu-id="6be48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be48-116">-DefaultProfile</span></span>
<span data-ttu-id="6be48-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6be48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be48-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6be48-118">-InputObject</span></span>
<span data-ttu-id="6be48-119">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="6be48-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6be48-120">-Name</span></span>
<span data-ttu-id="6be48-121">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="6be48-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be48-122">-ResourceGroupName</span></span>
<span data-ttu-id="6be48-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6be48-123">Resource group name.</span></span>

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

### <span data-ttu-id="6be48-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6be48-124">-ResourceId</span></span>
<span data-ttu-id="6be48-125">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6be48-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6be48-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6be48-126">-WorkspaceName</span></span>
<span data-ttu-id="6be48-127">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6be48-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6be48-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6be48-128">-WorkspaceObject</span></span>
<span data-ttu-id="6be48-129">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="6be48-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6be48-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be48-130">CommonParameters</span></span>
<span data-ttu-id="6be48-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be48-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be48-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6be48-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be48-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6be48-133">INPUTS</span></span>

### <span data-ttu-id="6be48-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6be48-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6be48-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6be48-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6be48-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be48-136">OUTPUTS</span></span>

### <span data-ttu-id="6be48-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="6be48-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="6be48-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6be48-138">NOTES</span></span>

## <span data-ttu-id="6be48-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6be48-139">RELATED LINKS</span></span>
