---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365551"
---
# <span data-ttu-id="c0aec-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c0aec-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="c0aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0aec-102">SYNOPSIS</span></span>
<span data-ttu-id="c0aec-103">Get-AzLoadBalancerBackendAddressPool egy vagy több háttércímkészletet ad vissza a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c0aec-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="c0aec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0aec-104">SYNTAX</span></span>

### <span data-ttu-id="c0aec-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0aec-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0aec-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0aec-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0aec-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0aec-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0aec-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0aec-108">DESCRIPTION</span></span>
<span data-ttu-id="c0aec-109">Get-AzLoadBalancerBackendAddressPool egy vagy több háttércímkészletet ad vissza a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c0aec-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="c0aec-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0aec-110">EXAMPLES</span></span>

### <span data-ttu-id="c0aec-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c0aec-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="c0aec-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c0aec-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="c0aec-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="c0aec-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="c0aec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0aec-114">PARAMETERS</span></span>

### <span data-ttu-id="c0aec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0aec-115">-DefaultProfile</span></span>
<span data-ttu-id="c0aec-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0aec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0aec-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c0aec-117">-LoadBalancer</span></span>
<span data-ttu-id="c0aec-118">{{ Fill LoadBalancer Description }}</span><span class="sxs-lookup"><span data-stu-id="c0aec-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="c0aec-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="c0aec-119">-LoadBalancerName</span></span>
<span data-ttu-id="c0aec-120">A terheléselosztás neve.</span><span class="sxs-lookup"><span data-stu-id="c0aec-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="c0aec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0aec-121">-Name</span></span>
<span data-ttu-id="c0aec-122">A háttércímkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="c0aec-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="c0aec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0aec-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0aec-124">A terheléselosztás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="c0aec-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="c0aec-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0aec-125">-ResourceId</span></span>

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

### <span data-ttu-id="c0aec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0aec-126">CommonParameters</span></span>
<span data-ttu-id="c0aec-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0aec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0aec-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0aec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0aec-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0aec-129">INPUTS</span></span>

### <span data-ttu-id="c0aec-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c0aec-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c0aec-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c0aec-131">System.String</span></span>

## <span data-ttu-id="c0aec-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0aec-132">OUTPUTS</span></span>

### <span data-ttu-id="c0aec-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c0aec-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c0aec-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0aec-134">NOTES</span></span>

## <span data-ttu-id="c0aec-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0aec-135">RELATED LINKS</span></span>
