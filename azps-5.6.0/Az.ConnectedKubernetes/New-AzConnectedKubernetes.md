---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: f6610b86f96602619f12323e7300c66ed39a9f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012502"
---
# <span data-ttu-id="806ae-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="806ae-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="806ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="806ae-102">SYNOPSIS</span></span>
<span data-ttu-id="806ae-103">API egy új K8s-fürt regisztrálásához és ezáltal egy nyomonott erőforrás létrehozásához a ARM</span><span class="sxs-lookup"><span data-stu-id="806ae-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="806ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="806ae-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="806ae-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="806ae-105">DESCRIPTION</span></span>
<span data-ttu-id="806ae-106">API egy új K8s-fürt regisztrálásához és ezáltal egy nyomonott erőforrás létrehozásához a ARM</span><span class="sxs-lookup"><span data-stu-id="806ae-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="806ae-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="806ae-107">EXAMPLES</span></span>

### <span data-ttu-id="806ae-108">1. példa: Csatlakoztatott kumernetes létrehozása</span><span class="sxs-lookup"><span data-stu-id="806ae-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="806ae-109">Ez a parancs csatlakoztatott rendszerhálózatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="806ae-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="806ae-110">1. példa: Csatlakoztatott, kubeConfig és kubeContext paramétereket is megszabadító kubeConfig és kubeContext paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="806ae-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="806ae-111">Ez a parancs egy kubeConfig és kubeContext paraméterekkel összekapcsolt kubeConfig és kubeContext paramétert is létrehoz.</span><span class="sxs-lookup"><span data-stu-id="806ae-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="806ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="806ae-112">PARAMETERS</span></span>

### <span data-ttu-id="806ae-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="806ae-113">-ClusterName</span></span>
<span data-ttu-id="806ae-114">Annak a Kutbernetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="806ae-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806ae-115">-DefaultProfile</span></span>
<span data-ttu-id="806ae-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="806ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806ae-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="806ae-117">-KubeConfig</span></span>
<span data-ttu-id="806ae-118">A kube config fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="806ae-118">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806ae-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="806ae-119">-KubeContext</span></span>
<span data-ttu-id="806ae-120">Az aktuális gépről származó Kubaconfig környezet</span><span class="sxs-lookup"><span data-stu-id="806ae-120">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806ae-121">-Location</span><span class="sxs-lookup"><span data-stu-id="806ae-121">-Location</span></span>
<span data-ttu-id="806ae-122">A fürt helye</span><span class="sxs-lookup"><span data-stu-id="806ae-122">Location of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="806ae-124">Annak az erőforráscsoportnak a neve, amelyhez a csapathálózati fürt regisztrálva van.</span><span class="sxs-lookup"><span data-stu-id="806ae-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806ae-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="806ae-125">-SubscriptionId</span></span>
<span data-ttu-id="806ae-126">Annak az előfizetésnek az azonosítója, amelyhez a többhálózati fürt regisztrálva van.</span><span class="sxs-lookup"><span data-stu-id="806ae-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806ae-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="806ae-127">-Confirm</span></span>
<span data-ttu-id="806ae-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="806ae-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="806ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="806ae-129">-WhatIf</span></span>
<span data-ttu-id="806ae-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="806ae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="806ae-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="806ae-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="806ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806ae-132">CommonParameters</span></span>
<span data-ttu-id="806ae-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806ae-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="806ae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806ae-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="806ae-135">INPUTS</span></span>

## <span data-ttu-id="806ae-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="806ae-136">OUTPUTS</span></span>

### <span data-ttu-id="806ae-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="806ae-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="806ae-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="806ae-138">NOTES</span></span>

<span data-ttu-id="806ae-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="806ae-139">ALIASES</span></span>

## <span data-ttu-id="806ae-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="806ae-140">RELATED LINKS</span></span>

