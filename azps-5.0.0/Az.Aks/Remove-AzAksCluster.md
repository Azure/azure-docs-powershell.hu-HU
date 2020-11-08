---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187107"
---
# <span data-ttu-id="71bf2-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="71bf2-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="71bf2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="71bf2-103">Felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="71bf2-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="71bf2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71bf2-104">SYNTAX</span></span>

### <span data-ttu-id="71bf2-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71bf2-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71bf2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71bf2-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71bf2-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71bf2-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71bf2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="71bf2-108">DESCRIPTION</span></span>
<span data-ttu-id="71bf2-109">Felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="71bf2-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="71bf2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="71bf2-110">EXAMPLES</span></span>

### <span data-ttu-id="71bf2-111">Meglévő felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="71bf2-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="71bf2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71bf2-112">PARAMETERS</span></span>

### <span data-ttu-id="71bf2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71bf2-113">-AsJob</span></span>
<span data-ttu-id="71bf2-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71bf2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71bf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71bf2-115">-DefaultProfile</span></span>
<span data-ttu-id="71bf2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71bf2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71bf2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="71bf2-117">-Force</span></span>
<span data-ttu-id="71bf2-118">Felügyelt Kubernetes-fürt eltávolítása üzenet nélkül</span><span class="sxs-lookup"><span data-stu-id="71bf2-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="71bf2-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="71bf2-119">-Id</span></span>
<span data-ttu-id="71bf2-120">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="71bf2-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="71bf2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71bf2-121">-InputObject</span></span>
<span data-ttu-id="71bf2-122">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="71bf2-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="71bf2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71bf2-123">-Name</span></span>
<span data-ttu-id="71bf2-124">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="71bf2-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="71bf2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71bf2-125">-PassThru</span></span>
<span data-ttu-id="71bf2-126">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="71bf2-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="71bf2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71bf2-127">-ResourceGroupName</span></span>
<span data-ttu-id="71bf2-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="71bf2-128">Resource group name</span></span>

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

### <span data-ttu-id="71bf2-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71bf2-129">-Confirm</span></span>
<span data-ttu-id="71bf2-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71bf2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71bf2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71bf2-131">-WhatIf</span></span>
<span data-ttu-id="71bf2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71bf2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71bf2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71bf2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71bf2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bf2-134">CommonParameters</span></span>
<span data-ttu-id="71bf2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71bf2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bf2-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="71bf2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bf2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71bf2-137">INPUTS</span></span>

### <span data-ttu-id="71bf2-138">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="71bf2-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="71bf2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="71bf2-139">System.String</span></span>

## <span data-ttu-id="71bf2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71bf2-140">OUTPUTS</span></span>

### <span data-ttu-id="71bf2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71bf2-141">System.Boolean</span></span>

## <span data-ttu-id="71bf2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71bf2-142">NOTES</span></span>

## <span data-ttu-id="71bf2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71bf2-143">RELATED LINKS</span></span>
