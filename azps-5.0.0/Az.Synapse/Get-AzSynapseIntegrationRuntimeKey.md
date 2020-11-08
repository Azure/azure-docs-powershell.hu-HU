---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185996"
---
# <span data-ttu-id="6670c-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6670c-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="6670c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6670c-102">SYNOPSIS</span></span>
<span data-ttu-id="6670c-103">Egy önállóan működtetett integrációs futásidejű kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="6670c-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="6670c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6670c-104">SYNTAX</span></span>

### <span data-ttu-id="6670c-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6670c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6670c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6670c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6670c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6670c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6670c-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6670c-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6670c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6670c-109">DESCRIPTION</span></span>
<span data-ttu-id="6670c-110">A **Get-AzSynapseIntegrationRuntimeKey** parancsmag az integrációs futtatókörnyezet kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6670c-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="6670c-111">A kulcsok az integrációs futásidejű csomópontok regisztrálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="6670c-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="6670c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="6670c-112">EXAMPLES</span></span>

### <span data-ttu-id="6670c-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6670c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="6670c-114">A parancsmag a ' teszt-selfhost-IR ' nevű integrációs futásidejű kulcsait keresi meg.</span><span class="sxs-lookup"><span data-stu-id="6670c-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6670c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6670c-115">PARAMETERS</span></span>

### <span data-ttu-id="6670c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6670c-116">-DefaultProfile</span></span>
<span data-ttu-id="6670c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6670c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6670c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6670c-118">-InputObject</span></span>
<span data-ttu-id="6670c-119">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="6670c-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="6670c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6670c-120">-Name</span></span>
<span data-ttu-id="6670c-121">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="6670c-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="6670c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6670c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6670c-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6670c-123">Resource group name.</span></span>

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

### <span data-ttu-id="6670c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6670c-124">-ResourceId</span></span>
<span data-ttu-id="6670c-125">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6670c-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6670c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6670c-126">-WorkspaceName</span></span>
<span data-ttu-id="6670c-127">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="6670c-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6670c-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6670c-128">-WorkspaceObject</span></span>
<span data-ttu-id="6670c-129">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="6670c-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6670c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6670c-130">CommonParameters</span></span>
<span data-ttu-id="6670c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6670c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6670c-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6670c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6670c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6670c-133">INPUTS</span></span>

### <span data-ttu-id="6670c-134">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6670c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6670c-135">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6670c-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6670c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6670c-136">OUTPUTS</span></span>

### <span data-ttu-id="6670c-137">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="6670c-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="6670c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6670c-138">NOTES</span></span>

## <span data-ttu-id="6670c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6670c-139">RELATED LINKS</span></span>
