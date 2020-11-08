---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186752"
---
# <span data-ttu-id="c13c1-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="c13c1-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="c13c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c13c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c13c1-103">API egy új K8s-fürt regisztrálásához, és ezáltal egy követett erőforrás létrehozása a KARJÁN</span><span class="sxs-lookup"><span data-stu-id="c13c1-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c13c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c13c1-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c13c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c13c1-105">DESCRIPTION</span></span>
<span data-ttu-id="c13c1-106">API egy új K8s-fürt regisztrálásához, és ezáltal egy követett erőforrás létrehozása a KARJÁN</span><span class="sxs-lookup"><span data-stu-id="c13c1-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c13c1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c13c1-107">EXAMPLES</span></span>

### <span data-ttu-id="c13c1-108">Példa 1: összekapcsolt kubernetes létrehozása</span><span class="sxs-lookup"><span data-stu-id="c13c1-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="c13c1-109">A parancs létrehoz egy csatlakoztatott kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c13c1-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="c13c1-110">Példa 1: összekapcsolt kubernetes létrehozása paraméterekkel a kubeConfig és a kubeContext</span><span class="sxs-lookup"><span data-stu-id="c13c1-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="c13c1-111">Ez a parancs létrehoz egy csatlakoztatott kubernetes paramétereket a kubeConfig és a kubeContext.</span><span class="sxs-lookup"><span data-stu-id="c13c1-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="c13c1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c13c1-112">PARAMETERS</span></span>

### <span data-ttu-id="c13c1-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="c13c1-113">-ClusterName</span></span>
<span data-ttu-id="c13c1-114">Annak a Kubernetes-csoportnak a neve, amelybe a beszerzést kéri.</span><span class="sxs-lookup"><span data-stu-id="c13c1-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="c13c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c13c1-115">-DefaultProfile</span></span>
<span data-ttu-id="c13c1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c13c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c13c1-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="c13c1-117">-KubeConfig</span></span>
<span data-ttu-id="c13c1-118">A Kube konfigurációs fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="c13c1-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="c13c1-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="c13c1-119">-KubeContext</span></span>
<span data-ttu-id="c13c1-120">Kubconfig környezet az aktuális számítógépről</span><span class="sxs-lookup"><span data-stu-id="c13c1-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="c13c1-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="c13c1-121">-Location</span></span>
<span data-ttu-id="c13c1-122">A fürt helye</span><span class="sxs-lookup"><span data-stu-id="c13c1-122">Location of the cluster</span></span>

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

### <span data-ttu-id="c13c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c13c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="c13c1-124">Annak az erőforráscsoportnek a neve, amelyhez a kubernetes-fürtöt regisztrálták.</span><span class="sxs-lookup"><span data-stu-id="c13c1-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="c13c1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c13c1-125">-SubscriptionId</span></span>
<span data-ttu-id="c13c1-126">Annak az előfizetésnek az azonosítója, amelyhez a kubernetes-fürtöt regisztrálták.</span><span class="sxs-lookup"><span data-stu-id="c13c1-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="c13c1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c13c1-127">-Confirm</span></span>
<span data-ttu-id="c13c1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c13c1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c13c1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c13c1-129">-WhatIf</span></span>
<span data-ttu-id="c13c1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c13c1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c13c1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c13c1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c13c1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c13c1-132">CommonParameters</span></span>
<span data-ttu-id="c13c1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c13c1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c13c1-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c13c1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c13c1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c13c1-135">INPUTS</span></span>

## <span data-ttu-id="c13c1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c13c1-136">OUTPUTS</span></span>

### <span data-ttu-id="c13c1-137">Microsoft. Azure. PowerShell. parancsmagok. ConnectedKubernetes. modellek. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="c13c1-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="c13c1-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c13c1-138">NOTES</span></span>

<span data-ttu-id="c13c1-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c13c1-139">ALIASES</span></span>

## <span data-ttu-id="c13c1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c13c1-140">RELATED LINKS</span></span>

