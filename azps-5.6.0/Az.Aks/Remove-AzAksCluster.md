---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: 0f0a1c530e4f02e031307006c0e6bf994f9a7c5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924289"
---
# <span data-ttu-id="c7302-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="c7302-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="c7302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7302-102">SYNOPSIS</span></span>
<span data-ttu-id="c7302-103">Felügyelt Kuternetes-fürt törlése.</span><span class="sxs-lookup"><span data-stu-id="c7302-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c7302-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7302-104">SYNTAX</span></span>

### <span data-ttu-id="c7302-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7302-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7302-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7302-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7302-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7302-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7302-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7302-108">DESCRIPTION</span></span>
<span data-ttu-id="c7302-109">Felügyelt Kuternetes-fürt törlése.</span><span class="sxs-lookup"><span data-stu-id="c7302-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c7302-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7302-110">EXAMPLES</span></span>

### <span data-ttu-id="c7302-111">Meglévő felügyelt Kubanetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="c7302-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="c7302-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7302-112">PARAMETERS</span></span>

### <span data-ttu-id="c7302-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7302-113">-AsJob</span></span>
<span data-ttu-id="c7302-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c7302-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7302-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7302-115">-DefaultProfile</span></span>
<span data-ttu-id="c7302-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7302-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7302-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c7302-117">-Force</span></span>
<span data-ttu-id="c7302-118">Felügyelt Kubanetes-fürt eltávolítása kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="c7302-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="c7302-119">-Id</span><span class="sxs-lookup"><span data-stu-id="c7302-119">-Id</span></span>
<span data-ttu-id="c7302-120">Felügyelt Kubanetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="c7302-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c7302-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7302-121">-InputObject</span></span>
<span data-ttu-id="c7302-122">EGY PSKubernetesCluster-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="c7302-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7302-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c7302-123">-Name</span></span>
<span data-ttu-id="c7302-124">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="c7302-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c7302-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7302-125">-PassThru</span></span>
<span data-ttu-id="c7302-126">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="c7302-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="c7302-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7302-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7302-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c7302-128">Resource group name</span></span>

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

### <span data-ttu-id="c7302-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7302-129">-Confirm</span></span>
<span data-ttu-id="c7302-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c7302-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7302-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7302-131">-WhatIf</span></span>
<span data-ttu-id="c7302-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c7302-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7302-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7302-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7302-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7302-134">CommonParameters</span></span>
<span data-ttu-id="c7302-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7302-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7302-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7302-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7302-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7302-137">INPUTS</span></span>

### <span data-ttu-id="c7302-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c7302-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c7302-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c7302-139">System.String</span></span>

## <span data-ttu-id="c7302-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7302-140">OUTPUTS</span></span>

### <span data-ttu-id="c7302-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c7302-141">System.Boolean</span></span>

## <span data-ttu-id="c7302-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7302-142">NOTES</span></span>

## <span data-ttu-id="c7302-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7302-143">RELATED LINKS</span></span>
