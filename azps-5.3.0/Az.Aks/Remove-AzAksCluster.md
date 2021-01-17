---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469122"
---
# <span data-ttu-id="6cfe5-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="6cfe5-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="6cfe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cfe5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfe5-103">Felügyelt Kuternetes-fürt törlése.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="6cfe5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cfe5-104">SYNTAX</span></span>

### <span data-ttu-id="6cfe5-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cfe5-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cfe5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cfe5-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cfe5-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cfe5-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cfe5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cfe5-108">DESCRIPTION</span></span>
<span data-ttu-id="6cfe5-109">Felügyelt Kuternetes-fürt törlése.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="6cfe5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cfe5-110">EXAMPLES</span></span>

### <span data-ttu-id="6cfe5-111">Meglévő felügyelt Kubanetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="6cfe5-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="6cfe5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cfe5-112">PARAMETERS</span></span>

### <span data-ttu-id="6cfe5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cfe5-113">-AsJob</span></span>
<span data-ttu-id="6cfe5-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6cfe5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cfe5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfe5-115">-DefaultProfile</span></span>
<span data-ttu-id="6cfe5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cfe5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6cfe5-117">-Force</span></span>
<span data-ttu-id="6cfe5-118">Felügyelt Kubanetes-fürt eltávolítása kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="6cfe5-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="6cfe5-119">-Id</span><span class="sxs-lookup"><span data-stu-id="6cfe5-119">-Id</span></span>
<span data-ttu-id="6cfe5-120">Felügyelt Kubanetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="6cfe5-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6cfe5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cfe5-121">-InputObject</span></span>
<span data-ttu-id="6cfe5-122">EGY PSKubernetesCluster-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6cfe5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6cfe5-123">-Name</span></span>
<span data-ttu-id="6cfe5-124">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="6cfe5-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6cfe5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cfe5-125">-PassThru</span></span>
<span data-ttu-id="6cfe5-126">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="6cfe5-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="6cfe5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfe5-127">-ResourceGroupName</span></span>
<span data-ttu-id="6cfe5-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6cfe5-128">Resource group name</span></span>

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

### <span data-ttu-id="6cfe5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cfe5-129">-Confirm</span></span>
<span data-ttu-id="6cfe5-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cfe5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cfe5-131">-WhatIf</span></span>
<span data-ttu-id="6cfe5-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cfe5-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cfe5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfe5-134">CommonParameters</span></span>
<span data-ttu-id="6cfe5-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfe5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfe5-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cfe5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfe5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cfe5-137">INPUTS</span></span>

### <span data-ttu-id="6cfe5-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6cfe5-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="6cfe5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6cfe5-139">System.String</span></span>

## <span data-ttu-id="6cfe5-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cfe5-140">OUTPUTS</span></span>

### <span data-ttu-id="6cfe5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6cfe5-141">System.Boolean</span></span>

## <span data-ttu-id="6cfe5-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cfe5-142">NOTES</span></span>

## <span data-ttu-id="6cfe5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cfe5-143">RELATED LINKS</span></span>
