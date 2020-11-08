---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018031"
---
# <span data-ttu-id="ad428-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="ad428-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="ad428-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad428-102">SYNOPSIS</span></span>
<span data-ttu-id="ad428-103">Tiltsa le az AK-bővítményeket.</span><span class="sxs-lookup"><span data-stu-id="ad428-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="ad428-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad428-104">SYNTAX</span></span>

### <span data-ttu-id="ad428-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad428-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad428-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad428-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad428-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad428-107">DESCRIPTION</span></span>
<span data-ttu-id="ad428-108">Tiltsa le az AK-bővítményeket.</span><span class="sxs-lookup"><span data-stu-id="ad428-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="ad428-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ad428-109">EXAMPLES</span></span>

### <span data-ttu-id="ad428-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad428-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="ad428-111">Tiltsa le a bővítményeket, `HttpApplicationRouting` `Monitoring` `AzurePolicy` `VirtualNode` és `KubeDashboard` az AK-ot.</span><span class="sxs-lookup"><span data-stu-id="ad428-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="ad428-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad428-112">PARAMETERS</span></span>

### <span data-ttu-id="ad428-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="ad428-113">-ClusterName</span></span>
<span data-ttu-id="ad428-114">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="ad428-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad428-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="ad428-115">-ClusterObject</span></span>
<span data-ttu-id="ad428-116">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ad428-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ad428-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad428-117">-DefaultProfile</span></span>
<span data-ttu-id="ad428-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad428-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad428-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad428-119">-Name</span></span>
<span data-ttu-id="ad428-120">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="ad428-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad428-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad428-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad428-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ad428-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad428-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad428-123">-Confirm</span></span>
<span data-ttu-id="ad428-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad428-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad428-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad428-125">-WhatIf</span></span>
<span data-ttu-id="ad428-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad428-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad428-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad428-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad428-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad428-128">CommonParameters</span></span>
<span data-ttu-id="ad428-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad428-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad428-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad428-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad428-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad428-131">INPUTS</span></span>

### <span data-ttu-id="ad428-132">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ad428-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ad428-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ad428-133">System.String</span></span>

## <span data-ttu-id="ad428-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad428-134">OUTPUTS</span></span>

### <span data-ttu-id="ad428-135">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ad428-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ad428-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad428-136">NOTES</span></span>

## <span data-ttu-id="ad428-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad428-137">RELATED LINKS</span></span>
