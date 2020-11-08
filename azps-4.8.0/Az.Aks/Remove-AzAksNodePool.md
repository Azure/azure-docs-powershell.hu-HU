---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180683"
---
# <span data-ttu-id="9f009-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="9f009-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="9f009-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f009-102">SYNOPSIS</span></span>
<span data-ttu-id="9f009-103">Csomópont-készlet törlése a felügyelt fürtből</span><span class="sxs-lookup"><span data-stu-id="9f009-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="9f009-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f009-104">SYNTAX</span></span>

### <span data-ttu-id="9f009-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f009-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f009-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f009-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f009-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f009-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f009-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f009-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f009-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f009-109">DESCRIPTION</span></span>
<span data-ttu-id="9f009-110">Csomópont-készlet törlése a felügyelt fürtből</span><span class="sxs-lookup"><span data-stu-id="9f009-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="9f009-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9f009-111">EXAMPLES</span></span>

### <span data-ttu-id="9f009-112">A megadott Node-készlet törlése</span><span class="sxs-lookup"><span data-stu-id="9f009-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="9f009-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f009-113">PARAMETERS</span></span>

### <span data-ttu-id="9f009-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f009-114">-AsJob</span></span>
<span data-ttu-id="9f009-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9f009-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f009-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="9f009-116">-ClusterName</span></span>
<span data-ttu-id="9f009-117">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="9f009-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="9f009-118">-ClusterObject</span></span>
<span data-ttu-id="9f009-119">A cluster objektum.</span><span class="sxs-lookup"><span data-stu-id="9f009-119">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f009-120">-DefaultProfile</span></span>
<span data-ttu-id="9f009-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f009-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f009-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9f009-122">-Force</span></span>
<span data-ttu-id="9f009-123">Csomópont-készlet eltávolítása a kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="9f009-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="9f009-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9f009-124">-Id</span></span>
<span data-ttu-id="9f009-125">Node-készlet azonosítója a felügyelt Kubernetes-fürtben</span><span class="sxs-lookup"><span data-stu-id="9f009-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f009-126">-InputObject</span></span>
<span data-ttu-id="9f009-127">Egy PSAgentPool objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9f009-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f009-128">-Name</span></span>
<span data-ttu-id="9f009-129">A Node-készlet neve</span><span class="sxs-lookup"><span data-stu-id="9f009-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f009-130">-PassThru</span></span>
<span data-ttu-id="9f009-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9f009-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9f009-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f009-132">-ResourceGroupName</span></span>
<span data-ttu-id="9f009-133">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9f009-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f009-134">-Confirm</span></span>
<span data-ttu-id="9f009-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f009-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f009-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f009-136">-WhatIf</span></span>
<span data-ttu-id="9f009-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f009-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f009-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f009-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f009-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f009-139">CommonParameters</span></span>
<span data-ttu-id="9f009-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f009-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f009-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f009-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f009-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f009-142">INPUTS</span></span>

### <span data-ttu-id="9f009-143">Microsoft. Azure. Command. AK. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="9f009-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="9f009-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9f009-144">System.String</span></span>

## <span data-ttu-id="9f009-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f009-145">OUTPUTS</span></span>

### <span data-ttu-id="9f009-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f009-146">System.Boolean</span></span>

## <span data-ttu-id="9f009-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f009-147">NOTES</span></span>

## <span data-ttu-id="9f009-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f009-148">RELATED LINKS</span></span>
