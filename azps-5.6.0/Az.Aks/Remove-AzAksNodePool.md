---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 27de96fccf2c420bd15e4a7522fecc16fd3032fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939793"
---
# <span data-ttu-id="30af1-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="30af1-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="30af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30af1-102">SYNOPSIS</span></span>
<span data-ttu-id="30af1-103">Csomópontkészlet törlése a felügyelt fürtből.</span><span class="sxs-lookup"><span data-stu-id="30af1-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="30af1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30af1-104">SYNTAX</span></span>

### <span data-ttu-id="30af1-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30af1-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30af1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30af1-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30af1-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30af1-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30af1-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30af1-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30af1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30af1-109">DESCRIPTION</span></span>
<span data-ttu-id="30af1-110">Csomópontkészlet törlése a felügyelt fürtből.</span><span class="sxs-lookup"><span data-stu-id="30af1-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="30af1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30af1-111">EXAMPLES</span></span>

### <span data-ttu-id="30af1-112">A megadott csomópontkészlet törlése</span><span class="sxs-lookup"><span data-stu-id="30af1-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="30af1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30af1-113">PARAMETERS</span></span>

### <span data-ttu-id="30af1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30af1-114">-AsJob</span></span>
<span data-ttu-id="30af1-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="30af1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30af1-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30af1-116">-ClusterName</span></span>
<span data-ttu-id="30af1-117">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="30af1-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="30af1-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="30af1-118">-ClusterObject</span></span>
<span data-ttu-id="30af1-119">A fürtobjektum.</span><span class="sxs-lookup"><span data-stu-id="30af1-119">The cluster object.</span></span>

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

### <span data-ttu-id="30af1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30af1-120">-DefaultProfile</span></span>
<span data-ttu-id="30af1-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30af1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30af1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="30af1-122">-Force</span></span>
<span data-ttu-id="30af1-123">Csomópontkészlet eltávolítása kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="30af1-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="30af1-124">-Id</span><span class="sxs-lookup"><span data-stu-id="30af1-124">-Id</span></span>
<span data-ttu-id="30af1-125">A felügyelt Kubanetes-fürtben található csomópontkészlet azonosítója</span><span class="sxs-lookup"><span data-stu-id="30af1-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="30af1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30af1-126">-InputObject</span></span>
<span data-ttu-id="30af1-127">EGY PSAgentPool-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="30af1-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="30af1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="30af1-128">-Name</span></span>
<span data-ttu-id="30af1-129">A csomópontkészlet neve</span><span class="sxs-lookup"><span data-stu-id="30af1-129">Name of your node pool</span></span>

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

### <span data-ttu-id="30af1-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30af1-130">-PassThru</span></span>
<span data-ttu-id="30af1-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="30af1-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="30af1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30af1-132">-ResourceGroupName</span></span>
<span data-ttu-id="30af1-133">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="30af1-133">Resource group name</span></span>

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

### <span data-ttu-id="30af1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30af1-134">-Confirm</span></span>
<span data-ttu-id="30af1-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="30af1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30af1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30af1-136">-WhatIf</span></span>
<span data-ttu-id="30af1-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="30af1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30af1-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30af1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30af1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30af1-139">CommonParameters</span></span>
<span data-ttu-id="30af1-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30af1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30af1-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30af1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30af1-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30af1-142">INPUTS</span></span>

### <span data-ttu-id="30af1-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="30af1-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="30af1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="30af1-144">System.String</span></span>

## <span data-ttu-id="30af1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30af1-145">OUTPUTS</span></span>

### <span data-ttu-id="30af1-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30af1-146">System.Boolean</span></span>

## <span data-ttu-id="30af1-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30af1-147">NOTES</span></span>

## <span data-ttu-id="30af1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30af1-148">RELATED LINKS</span></span>
