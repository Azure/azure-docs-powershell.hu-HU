---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 5d0cc543d5ec893ecb1f83b8fd62f25bcb32f5b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926098"
---
# <span data-ttu-id="3f8cb-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="3f8cb-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="3f8cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8cb-103">Tiltsa le a bővítményeket a ékek számára.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="3f8cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f8cb-104">SYNTAX</span></span>

### <span data-ttu-id="3f8cb-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f8cb-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f8cb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f8cb-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f8cb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f8cb-107">DESCRIPTION</span></span>
<span data-ttu-id="3f8cb-108">Tiltsa le a bővítményeket a ékek számára.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="3f8cb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f8cb-109">EXAMPLES</span></span>

### <span data-ttu-id="3f8cb-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="3f8cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="3f8cb-111">Tiltsa le a `HttpApplicationRouting` `Monitoring` bővítményeket, `AzurePolicy` a , és a `VirtualNode` `KubeDashboard` festékeket.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="3f8cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f8cb-112">PARAMETERS</span></span>

### <span data-ttu-id="3f8cb-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3f8cb-113">-ClusterName</span></span>
<span data-ttu-id="3f8cb-114">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="3f8cb-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="3f8cb-115">-ClusterObject</span></span>
<span data-ttu-id="3f8cb-116">EGY PSKubernetesCluster-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3f8cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8cb-117">-DefaultProfile</span></span>
<span data-ttu-id="3f8cb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f8cb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3f8cb-119">-Name</span></span>
<span data-ttu-id="3f8cb-120">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="3f8cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f8cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="3f8cb-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3f8cb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f8cb-123">-Confirm</span></span>
<span data-ttu-id="3f8cb-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f8cb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f8cb-125">-WhatIf</span></span>
<span data-ttu-id="3f8cb-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f8cb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f8cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8cb-128">CommonParameters</span></span>
<span data-ttu-id="3f8cb-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8cb-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f8cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8cb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f8cb-131">INPUTS</span></span>

### <span data-ttu-id="3f8cb-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="3f8cb-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="3f8cb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3f8cb-133">System.String</span></span>

## <span data-ttu-id="3f8cb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f8cb-134">OUTPUTS</span></span>

### <span data-ttu-id="3f8cb-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="3f8cb-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="3f8cb-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f8cb-136">NOTES</span></span>

## <span data-ttu-id="3f8cb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f8cb-137">RELATED LINKS</span></span>
