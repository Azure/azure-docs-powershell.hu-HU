---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 40fb9f328f0f838f5d76de6de5509c74b0002768
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167139"
---
# <span data-ttu-id="c3dd1-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="c3dd1-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="c3dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="c3dd1-103">Engedélyezze a bővítményeket a ékek számára.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="c3dd1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3dd1-104">SYNTAX</span></span>

### <span data-ttu-id="c3dd1-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3dd1-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3dd1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3dd1-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3dd1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3dd1-107">DESCRIPTION</span></span>
<span data-ttu-id="c3dd1-108">Engedélyezze a bővítményeket a ékek számára.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="c3dd1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3dd1-109">EXAMPLES</span></span>

### <span data-ttu-id="c3dd1-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3dd1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="c3dd1-111">Engedélyezze a `HttpApplicationRouting` bővítményeket, a , és a `Monitoring` `AzurePolicy` `VirtualNode` `KubeDashboard` ékeket.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="c3dd1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3dd1-112">PARAMETERS</span></span>

### <span data-ttu-id="c3dd1-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c3dd1-113">-ClusterName</span></span>
<span data-ttu-id="c3dd1-114">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="c3dd1-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="c3dd1-115">-ClusterObject</span></span>
<span data-ttu-id="c3dd1-116">EGY PSKubernetesCluster-objektum, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c3dd1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3dd1-117">-DefaultProfile</span></span>
<span data-ttu-id="c3dd1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3dd1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c3dd1-119">-Name</span></span>
<span data-ttu-id="c3dd1-120">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="c3dd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3dd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3dd1-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c3dd1-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c3dd1-123">-SubnetName</span></span>
<span data-ttu-id="c3dd1-124">A VirtualNode alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="c3dd1-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="c3dd1-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="c3dd1-126">A figyelési munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="c3dd1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3dd1-127">-Confirm</span></span>
<span data-ttu-id="c3dd1-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3dd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3dd1-129">-WhatIf</span></span>
<span data-ttu-id="c3dd1-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3dd1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3dd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3dd1-132">CommonParameters</span></span>
<span data-ttu-id="c3dd1-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3dd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3dd1-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3dd1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3dd1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3dd1-135">INPUTS</span></span>

### <span data-ttu-id="c3dd1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c3dd1-136">System.String</span></span>

### <span data-ttu-id="c3dd1-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c3dd1-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c3dd1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3dd1-138">OUTPUTS</span></span>

### <span data-ttu-id="c3dd1-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c3dd1-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c3dd1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3dd1-140">NOTES</span></span>

## <span data-ttu-id="c3dd1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3dd1-141">RELATED LINKS</span></span>
