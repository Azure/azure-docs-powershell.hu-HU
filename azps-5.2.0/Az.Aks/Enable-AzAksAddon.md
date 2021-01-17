---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342486"
---
# <span data-ttu-id="94c99-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="94c99-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="94c99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c99-102">SYNOPSIS</span></span>
<span data-ttu-id="94c99-103">Engedélyezze a bővítményeket a ékek számára.</span><span class="sxs-lookup"><span data-stu-id="94c99-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="94c99-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94c99-104">SYNTAX</span></span>

### <span data-ttu-id="94c99-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94c99-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94c99-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94c99-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94c99-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94c99-107">DESCRIPTION</span></span>
<span data-ttu-id="94c99-108">Engedélyezze a bővítményeket a ékek számára.</span><span class="sxs-lookup"><span data-stu-id="94c99-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="94c99-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94c99-109">EXAMPLES</span></span>

### <span data-ttu-id="94c99-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="94c99-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="94c99-111">Engedélyezze a `HttpApplicationRouting` `Monitoring` bővítményeket, `AzurePolicy` a , és a `VirtualNode` `KubeDashboard` ékeket.</span><span class="sxs-lookup"><span data-stu-id="94c99-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="94c99-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94c99-112">PARAMETERS</span></span>

### <span data-ttu-id="94c99-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94c99-113">-ClusterName</span></span>
<span data-ttu-id="94c99-114">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="94c99-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="94c99-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="94c99-115">-ClusterObject</span></span>
<span data-ttu-id="94c99-116">EGY PSKubernetesCluster-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="94c99-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="94c99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c99-117">-DefaultProfile</span></span>
<span data-ttu-id="94c99-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94c99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c99-119">-Name</span><span class="sxs-lookup"><span data-stu-id="94c99-119">-Name</span></span>
<span data-ttu-id="94c99-120">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="94c99-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="94c99-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c99-121">-ResourceGroupName</span></span>
<span data-ttu-id="94c99-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94c99-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="94c99-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="94c99-123">-SubnetName</span></span>
<span data-ttu-id="94c99-124">A VirtualNode alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="94c99-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c99-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="94c99-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="94c99-126">A figyelési munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94c99-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c99-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94c99-127">-Confirm</span></span>
<span data-ttu-id="94c99-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94c99-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c99-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c99-129">-WhatIf</span></span>
<span data-ttu-id="94c99-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94c99-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c99-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94c99-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c99-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c99-132">CommonParameters</span></span>
<span data-ttu-id="94c99-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c99-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c99-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94c99-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c99-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94c99-135">INPUTS</span></span>

### <span data-ttu-id="94c99-136">System.String</span><span class="sxs-lookup"><span data-stu-id="94c99-136">System.String</span></span>

### <span data-ttu-id="94c99-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="94c99-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="94c99-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94c99-138">OUTPUTS</span></span>

### <span data-ttu-id="94c99-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="94c99-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="94c99-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94c99-140">NOTES</span></span>

## <span data-ttu-id="94c99-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94c99-141">RELATED LINKS</span></span>
