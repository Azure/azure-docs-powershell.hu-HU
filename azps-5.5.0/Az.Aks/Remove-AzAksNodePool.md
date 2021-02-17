---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159883"
---
# <span data-ttu-id="1e6a9-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="1e6a9-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="1e6a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6a9-103">Csomópontkészlet törlése a felügyelt fürtből.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="1e6a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e6a9-104">SYNTAX</span></span>

### <span data-ttu-id="1e6a9-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e6a9-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e6a9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6a9-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e6a9-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6a9-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e6a9-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6a9-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e6a9-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e6a9-109">DESCRIPTION</span></span>
<span data-ttu-id="1e6a9-110">Csomópontkészlet törlése a felügyelt fürtből.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="1e6a9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e6a9-111">EXAMPLES</span></span>

### <span data-ttu-id="1e6a9-112">A megadott csomópontkészlet törlése</span><span class="sxs-lookup"><span data-stu-id="1e6a9-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="1e6a9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e6a9-113">PARAMETERS</span></span>

### <span data-ttu-id="1e6a9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e6a9-114">-AsJob</span></span>
<span data-ttu-id="1e6a9-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1e6a9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e6a9-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1e6a9-116">-ClusterName</span></span>
<span data-ttu-id="1e6a9-117">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="1e6a9-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="1e6a9-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="1e6a9-118">-ClusterObject</span></span>
<span data-ttu-id="1e6a9-119">A fürtobjektum.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-119">The cluster object.</span></span>

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

### <span data-ttu-id="1e6a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6a9-120">-DefaultProfile</span></span>
<span data-ttu-id="1e6a9-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e6a9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1e6a9-122">-Force</span></span>
<span data-ttu-id="1e6a9-123">Csomópontkészlet eltávolítása kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="1e6a9-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="1e6a9-124">-Id</span><span class="sxs-lookup"><span data-stu-id="1e6a9-124">-Id</span></span>
<span data-ttu-id="1e6a9-125">A felügyelt Kubanetes-fürtben található csomópontkészlet azonosítója</span><span class="sxs-lookup"><span data-stu-id="1e6a9-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="1e6a9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e6a9-126">-InputObject</span></span>
<span data-ttu-id="1e6a9-127">EGY PSAgentPool-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1e6a9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1e6a9-128">-Name</span></span>
<span data-ttu-id="1e6a9-129">A csomópontkészlet neve</span><span class="sxs-lookup"><span data-stu-id="1e6a9-129">Name of your node pool</span></span>

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

### <span data-ttu-id="1e6a9-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e6a9-130">-PassThru</span></span>
<span data-ttu-id="1e6a9-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="1e6a9-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1e6a9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6a9-132">-ResourceGroupName</span></span>
<span data-ttu-id="1e6a9-133">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1e6a9-133">Resource group name</span></span>

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

### <span data-ttu-id="1e6a9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e6a9-134">-Confirm</span></span>
<span data-ttu-id="1e6a9-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6a9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6a9-136">-WhatIf</span></span>
<span data-ttu-id="1e6a9-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e6a9-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e6a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6a9-139">CommonParameters</span></span>
<span data-ttu-id="1e6a9-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6a9-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e6a9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6a9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e6a9-142">INPUTS</span></span>

### <span data-ttu-id="1e6a9-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="1e6a9-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="1e6a9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1e6a9-144">System.String</span></span>

## <span data-ttu-id="1e6a9-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e6a9-145">OUTPUTS</span></span>

### <span data-ttu-id="1e6a9-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e6a9-146">System.Boolean</span></span>

## <span data-ttu-id="1e6a9-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e6a9-147">NOTES</span></span>

## <span data-ttu-id="1e6a9-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e6a9-148">RELATED LINKS</span></span>
