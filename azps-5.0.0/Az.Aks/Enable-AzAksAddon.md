---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187898"
---
# <span data-ttu-id="b257c-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="b257c-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="b257c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b257c-102">SYNOPSIS</span></span>
<span data-ttu-id="b257c-103">Engedélyezze a bővítmények az AK-hoz jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="b257c-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="b257c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b257c-104">SYNTAX</span></span>

### <span data-ttu-id="b257c-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b257c-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b257c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b257c-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b257c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b257c-107">DESCRIPTION</span></span>
<span data-ttu-id="b257c-108">Engedélyezze a bővítmények az AK-hoz jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="b257c-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="b257c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b257c-109">EXAMPLES</span></span>

### <span data-ttu-id="b257c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b257c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="b257c-111">Engedélyezze a bővítményeket, `HttpApplicationRouting` `Monitoring` `AzurePolicy` `VirtualNode` és `KubeDashboard` az AK-ot.</span><span class="sxs-lookup"><span data-stu-id="b257c-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="b257c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b257c-112">PARAMETERS</span></span>

### <span data-ttu-id="b257c-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b257c-113">-ClusterName</span></span>
<span data-ttu-id="b257c-114">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="b257c-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="b257c-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b257c-115">-ClusterObject</span></span>
<span data-ttu-id="b257c-116">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="b257c-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="b257c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b257c-117">-DefaultProfile</span></span>
<span data-ttu-id="b257c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b257c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b257c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b257c-119">-Name</span></span>
<span data-ttu-id="b257c-120">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="b257c-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="b257c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b257c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b257c-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b257c-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="b257c-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b257c-123">-SubnetName</span></span>
<span data-ttu-id="b257c-124">A VirtualNode alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="b257c-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="b257c-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b257c-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="b257c-126">A megfigyelési munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b257c-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="b257c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b257c-127">-Confirm</span></span>
<span data-ttu-id="b257c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b257c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b257c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b257c-129">-WhatIf</span></span>
<span data-ttu-id="b257c-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b257c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b257c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b257c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b257c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b257c-132">CommonParameters</span></span>
<span data-ttu-id="b257c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b257c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b257c-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b257c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b257c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b257c-135">INPUTS</span></span>

### <span data-ttu-id="b257c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b257c-136">System.String</span></span>

### <span data-ttu-id="b257c-137">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b257c-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b257c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b257c-138">OUTPUTS</span></span>

### <span data-ttu-id="b257c-139">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b257c-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b257c-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b257c-140">NOTES</span></span>

## <span data-ttu-id="b257c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b257c-141">RELATED LINKS</span></span>
