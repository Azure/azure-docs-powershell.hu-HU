---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017462"
---
# <span data-ttu-id="ee1b8-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="ee1b8-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="ee1b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1b8-103">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="ee1b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee1b8-104">SYNTAX</span></span>

### <span data-ttu-id="ee1b8-105">StopByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee1b8-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1b8-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1b8-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1b8-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1b8-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1b8-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1b8-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1b8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee1b8-109">DESCRIPTION</span></span>
<span data-ttu-id="ee1b8-110">A **szinkronizálás-AzSynapseIntegrationRuntimeCredential** parancsmag a helyszíni hitelesítő adatokat szinkronizálja az integrációs futásidejű csomópontok között, így a hitelesítő adatok mindegyik csomópontban azonosak lesznek.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="ee1b8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ee1b8-111">EXAMPLES</span></span>

### <span data-ttu-id="ee1b8-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ee1b8-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="ee1b8-113">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="ee1b8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee1b8-114">PARAMETERS</span></span>

### <span data-ttu-id="ee1b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1b8-115">-DefaultProfile</span></span>
<span data-ttu-id="ee1b8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1b8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ee1b8-117">-Force</span></span>
<span data-ttu-id="ee1b8-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ee1b8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee1b8-119">-InputObject</span></span>
<span data-ttu-id="ee1b8-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b8-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ee1b8-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ee1b8-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee1b8-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee1b8-125">-ResourceId</span></span>
<span data-ttu-id="ee1b8-126">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b8-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ee1b8-127">-WorkspaceName</span></span>
<span data-ttu-id="ee1b8-128">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b8-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ee1b8-129">-WorkspaceObject</span></span>
<span data-ttu-id="ee1b8-130">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b8-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee1b8-131">-Confirm</span></span>
<span data-ttu-id="ee1b8-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1b8-133">-WhatIf</span></span>
<span data-ttu-id="ee1b8-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1b8-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1b8-136">CommonParameters</span></span>
<span data-ttu-id="ee1b8-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee1b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1b8-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee1b8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1b8-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee1b8-139">INPUTS</span></span>

### <span data-ttu-id="ee1b8-140">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ee1b8-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ee1b8-141">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ee1b8-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ee1b8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee1b8-142">OUTPUTS</span></span>

### <span data-ttu-id="ee1b8-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="ee1b8-143">System.Void</span></span>

## <span data-ttu-id="ee1b8-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee1b8-144">NOTES</span></span>

## <span data-ttu-id="ee1b8-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee1b8-145">RELATED LINKS</span></span>
