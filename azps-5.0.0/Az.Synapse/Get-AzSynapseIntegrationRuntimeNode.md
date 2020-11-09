---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302366"
---
# <span data-ttu-id="5d84e-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5d84e-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="5d84e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d84e-102">SYNOPSIS</span></span>
<span data-ttu-id="5d84e-103">Beolvassa az integrációs futtatókörnyezet csomópontjának adatait.</span><span class="sxs-lookup"><span data-stu-id="5d84e-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="5d84e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d84e-104">SYNTAX</span></span>

### <span data-ttu-id="5d84e-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d84e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d84e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d84e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d84e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d84e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d84e-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d84e-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d84e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d84e-109">DESCRIPTION</span></span>
<span data-ttu-id="5d84e-110">A **Get-AzSynapseIntegrationRuntimeNode** parancsmag az integrációs futásidejű csomópontok részletes adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5d84e-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="5d84e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5d84e-111">EXAMPLES</span></span>

### <span data-ttu-id="5d84e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5d84e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="5d84e-113">A parancsmag az "Node_1" nevű csomópontról kapja az "tesztelje a selfhost-IR" nevű csomópontot a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5d84e-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5d84e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5d84e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="5d84e-115">A parancsmag az "Node_1" nevű csomópontról kapja a "teszt-selfhost-IR"-ban a munkaterület "teszt-DF-EU2" nevű csomópontját, az IP-címet is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="5d84e-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="5d84e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d84e-116">PARAMETERS</span></span>

### <span data-ttu-id="5d84e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d84e-117">-DefaultProfile</span></span>
<span data-ttu-id="5d84e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d84e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d84e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d84e-119">-InputObject</span></span>
<span data-ttu-id="5d84e-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="5d84e-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="5d84e-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5d84e-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5d84e-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="5d84e-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="5d84e-123">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="5d84e-123">-IpAddress</span></span>
<span data-ttu-id="5d84e-124">Az integrációs futásidejű csomópont IP-címe.</span><span class="sxs-lookup"><span data-stu-id="5d84e-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="5d84e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d84e-125">-Name</span></span>
<span data-ttu-id="5d84e-126">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="5d84e-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="5d84e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d84e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d84e-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5d84e-128">Resource group name.</span></span>

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

### <span data-ttu-id="5d84e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d84e-129">-ResourceId</span></span>
<span data-ttu-id="5d84e-130">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5d84e-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="5d84e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5d84e-131">-WorkspaceName</span></span>
<span data-ttu-id="5d84e-132">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="5d84e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d84e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5d84e-133">-WorkspaceObject</span></span>
<span data-ttu-id="5d84e-134">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="5d84e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5d84e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d84e-135">CommonParameters</span></span>
<span data-ttu-id="5d84e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d84e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d84e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d84e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d84e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d84e-138">INPUTS</span></span>

### <span data-ttu-id="5d84e-139">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d84e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5d84e-140">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5d84e-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5d84e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d84e-141">OUTPUTS</span></span>

### <span data-ttu-id="5d84e-142">Microsoft. Azure. commands. szinapszis. models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5d84e-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="5d84e-143">Microsoft. Azure. commands. szinapszis. models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5d84e-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="5d84e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d84e-144">NOTES</span></span>

## <span data-ttu-id="5d84e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d84e-145">RELATED LINKS</span></span>
