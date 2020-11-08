---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195203"
---
# <span data-ttu-id="20456-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="20456-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="20456-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20456-102">SYNOPSIS</span></span>
<span data-ttu-id="20456-103">Get-AzLoadBalancerBackendAddressPool beolvassa a terheléselosztó bővítményhez társított egy vagy több backend-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="20456-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="20456-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20456-104">SYNTAX</span></span>

### <span data-ttu-id="20456-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="20456-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20456-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20456-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20456-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20456-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20456-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="20456-108">DESCRIPTION</span></span>
<span data-ttu-id="20456-109">Get-AzLoadBalancerBackendAddressPool beolvassa a terheléselosztó bővítményhez társított egy vagy több backend-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="20456-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="20456-110">Példák</span><span class="sxs-lookup"><span data-stu-id="20456-110">EXAMPLES</span></span>

### <span data-ttu-id="20456-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="20456-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="20456-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="20456-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="20456-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="20456-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="20456-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20456-114">PARAMETERS</span></span>

### <span data-ttu-id="20456-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20456-115">-DefaultProfile</span></span>
<span data-ttu-id="20456-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20456-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20456-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20456-117">-LoadBalancer</span></span>
<span data-ttu-id="20456-118">{{Fill LoadBalancer Description}}</span><span class="sxs-lookup"><span data-stu-id="20456-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20456-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="20456-119">-LoadBalancerName</span></span>
<span data-ttu-id="20456-120">A terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="20456-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20456-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20456-121">-Name</span></span>
<span data-ttu-id="20456-122">A backend-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="20456-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20456-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20456-123">-ResourceGroupName</span></span>
<span data-ttu-id="20456-124">Az erőforráscsoport neve a terheléselosztó csoportban.</span><span class="sxs-lookup"><span data-stu-id="20456-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20456-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20456-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20456-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20456-126">CommonParameters</span></span>
<span data-ttu-id="20456-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20456-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20456-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="20456-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20456-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20456-129">INPUTS</span></span>

### <span data-ttu-id="20456-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20456-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="20456-131">System. String</span><span class="sxs-lookup"><span data-stu-id="20456-131">System.String</span></span>

## <span data-ttu-id="20456-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20456-132">OUTPUTS</span></span>

### <span data-ttu-id="20456-133">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="20456-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="20456-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20456-134">NOTES</span></span>

## <span data-ttu-id="20456-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20456-135">RELATED LINKS</span></span>
