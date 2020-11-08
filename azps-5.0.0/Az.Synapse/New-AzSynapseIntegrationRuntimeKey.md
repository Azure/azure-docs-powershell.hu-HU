---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187934"
---
# <span data-ttu-id="9f4f2-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="9f4f2-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="9f4f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4f2-103">Önkiszolgáló integrációs futásidejű kulcs újbóli létrehozása</span><span class="sxs-lookup"><span data-stu-id="9f4f2-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="9f4f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f4f2-104">SYNTAX</span></span>

### <span data-ttu-id="9f4f2-105">NewByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f4f2-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f4f2-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f4f2-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f4f2-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f4f2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f4f2-109">DESCRIPTION</span></span>
<span data-ttu-id="9f4f2-110">A **New-AzSynapseIntegrationRuntimeKey** parancsmag az integrációs futtatókörnyezetet az "kulcsnév" paraméter által megadott kulccsal hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="9f4f2-111">Az előző kulcs érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="9f4f2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9f4f2-112">EXAMPLES</span></span>

### <span data-ttu-id="9f4f2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9f4f2-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="9f4f2-114">A parancsmag újragenerálja a "authKey2" "selfhost-IR" nevű integrációs futásidejű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9f4f2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f4f2-115">PARAMETERS</span></span>

### <span data-ttu-id="9f4f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4f2-116">-DefaultProfile</span></span>
<span data-ttu-id="9f4f2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f4f2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9f4f2-118">-Force</span></span>
<span data-ttu-id="9f4f2-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9f4f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f4f2-120">-InputObject</span></span>
<span data-ttu-id="9f4f2-121">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f2-122">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="9f4f2-122">-KeyName</span></span>
<span data-ttu-id="9f4f2-123">Az önkiszolgáló integrációs futtatókörnyezet hitelesítő kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f4f2-124">-Name</span></span>
<span data-ttu-id="9f4f2-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f4f2-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f4f2-128">-ResourceId</span></span>
<span data-ttu-id="9f4f2-129">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f2-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-130">-WorkspaceName</span></span>
<span data-ttu-id="9f4f2-131">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f2-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9f4f2-132">-WorkspaceObject</span></span>
<span data-ttu-id="9f4f2-133">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f2-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f4f2-134">-Confirm</span></span>
<span data-ttu-id="9f4f2-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4f2-136">-WhatIf</span></span>
<span data-ttu-id="9f4f2-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f4f2-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4f2-139">CommonParameters</span></span>
<span data-ttu-id="9f4f2-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f4f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4f2-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4f2-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f4f2-142">INPUTS</span></span>

### <span data-ttu-id="9f4f2-143">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9f4f2-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9f4f2-144">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9f4f2-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9f4f2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f4f2-145">OUTPUTS</span></span>

### <span data-ttu-id="9f4f2-146">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="9f4f2-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="9f4f2-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f4f2-147">NOTES</span></span>

## <span data-ttu-id="9f4f2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f4f2-148">RELATED LINKS</span></span>