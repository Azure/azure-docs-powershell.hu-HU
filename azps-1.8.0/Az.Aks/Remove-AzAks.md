---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: dc8b22697d606e827a0855a446d969ff2c90edc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665747"
---
# <span data-ttu-id="37aed-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="37aed-101">Remove-AzAks</span></span>

## <span data-ttu-id="37aed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37aed-102">SYNOPSIS</span></span>
<span data-ttu-id="37aed-103">Felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="37aed-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="37aed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37aed-104">SYNTAX</span></span>

### <span data-ttu-id="37aed-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37aed-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37aed-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37aed-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37aed-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37aed-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37aed-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="37aed-108">DESCRIPTION</span></span>
<span data-ttu-id="37aed-109">Felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="37aed-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="37aed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="37aed-110">EXAMPLES</span></span>

### <span data-ttu-id="37aed-111">Meglévő felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="37aed-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="37aed-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37aed-112">PARAMETERS</span></span>

### <span data-ttu-id="37aed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37aed-113">-AsJob</span></span>
<span data-ttu-id="37aed-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="37aed-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37aed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37aed-115">-DefaultProfile</span></span>
<span data-ttu-id="37aed-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37aed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37aed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="37aed-117">-Force</span></span>
<span data-ttu-id="37aed-118">Felügyelt Kubernetes-fürt eltávolítása üzenet nélkül</span><span class="sxs-lookup"><span data-stu-id="37aed-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="37aed-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="37aed-119">-Id</span></span>
<span data-ttu-id="37aed-120">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="37aed-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="37aed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37aed-121">-InputObject</span></span>
<span data-ttu-id="37aed-122">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="37aed-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="37aed-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37aed-123">-Name</span></span>
<span data-ttu-id="37aed-124">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="37aed-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="37aed-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37aed-125">-PassThru</span></span>
<span data-ttu-id="37aed-126">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="37aed-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="37aed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37aed-127">-ResourceGroupName</span></span>
<span data-ttu-id="37aed-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="37aed-128">Resource group name</span></span>

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

### <span data-ttu-id="37aed-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="37aed-129">-Confirm</span></span>
<span data-ttu-id="37aed-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="37aed-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37aed-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37aed-131">-WhatIf</span></span>
<span data-ttu-id="37aed-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="37aed-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37aed-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37aed-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37aed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37aed-134">CommonParameters</span></span>
<span data-ttu-id="37aed-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37aed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37aed-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37aed-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37aed-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37aed-137">INPUTS</span></span>

### <span data-ttu-id="37aed-138">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="37aed-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="37aed-139">System. String</span><span class="sxs-lookup"><span data-stu-id="37aed-139">System.String</span></span>

## <span data-ttu-id="37aed-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37aed-140">OUTPUTS</span></span>

### <span data-ttu-id="37aed-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37aed-141">System.Boolean</span></span>

## <span data-ttu-id="37aed-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37aed-142">NOTES</span></span>

## <span data-ttu-id="37aed-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37aed-143">RELATED LINKS</span></span>
