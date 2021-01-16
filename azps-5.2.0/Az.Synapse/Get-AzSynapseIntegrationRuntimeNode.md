---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339198"
---
# <span data-ttu-id="37e8e-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="37e8e-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="37e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="37e8e-103">Integrációs futásidejű csomópontadatokat kap.</span><span class="sxs-lookup"><span data-stu-id="37e8e-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="37e8e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37e8e-104">SYNTAX</span></span>

### <span data-ttu-id="37e8e-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37e8e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37e8e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37e8e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37e8e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37e8e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37e8e-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37e8e-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37e8e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37e8e-109">DESCRIPTION</span></span>
<span data-ttu-id="37e8e-110">A **Get-AzSynapseIntegrationRuntimeNode** parancsmag megkapja az integrációs futásidejű csomópont részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="37e8e-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="37e8e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37e8e-111">EXAMPLES</span></span>

### <span data-ttu-id="37e8e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="37e8e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="37e8e-113">A parancsmag a ContosoWorkspace munkaterületén az "Node_1" nevű csomópont adatait kapja az önkiszolgáló integrációs futásidejű "test-selfhost-ir" környezetben.</span><span class="sxs-lookup"><span data-stu-id="37e8e-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="37e8e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="37e8e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="37e8e-115">A parancsmag a "test-df-eu2" munkaterület "test-df-eu2" nevű, önkiszolgáló integrációs futásidejű "test-selfhost-ir" "Node_1" nevű csomópontról kap információkat, az IP-címet is beleértve.</span><span class="sxs-lookup"><span data-stu-id="37e8e-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="37e8e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37e8e-116">PARAMETERS</span></span>

### <span data-ttu-id="37e8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e8e-117">-DefaultProfile</span></span>
<span data-ttu-id="37e8e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37e8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e8e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37e8e-119">-InputObject</span></span>
<span data-ttu-id="37e8e-120">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="37e8e-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="37e8e-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="37e8e-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="37e8e-122">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="37e8e-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="37e8e-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="37e8e-123">-IpAddress</span></span>
<span data-ttu-id="37e8e-124">Az integrációs futásidejű csomópont IP-címe.</span><span class="sxs-lookup"><span data-stu-id="37e8e-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="37e8e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="37e8e-125">-Name</span></span>
<span data-ttu-id="37e8e-126">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="37e8e-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e8e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e8e-127">-ResourceGroupName</span></span>
<span data-ttu-id="37e8e-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="37e8e-128">Resource group name.</span></span>

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

### <span data-ttu-id="37e8e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37e8e-129">-ResourceId</span></span>
<span data-ttu-id="37e8e-130">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="37e8e-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="37e8e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37e8e-131">-WorkspaceName</span></span>
<span data-ttu-id="37e8e-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="37e8e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="37e8e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="37e8e-133">-WorkspaceObject</span></span>
<span data-ttu-id="37e8e-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="37e8e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="37e8e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e8e-135">CommonParameters</span></span>
<span data-ttu-id="37e8e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e8e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e8e-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37e8e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e8e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37e8e-138">INPUTS</span></span>

### <span data-ttu-id="37e8e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="37e8e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="37e8e-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="37e8e-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="37e8e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37e8e-141">OUTPUTS</span></span>

### <span data-ttu-id="37e8e-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="37e8e-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="37e8e-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="37e8e-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="37e8e-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37e8e-144">NOTES</span></span>

## <span data-ttu-id="37e8e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37e8e-145">RELATED LINKS</span></span>
