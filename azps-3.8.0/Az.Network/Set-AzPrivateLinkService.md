---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013094"
---
# <span data-ttu-id="e0808-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e0808-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="e0808-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0808-102">SYNOPSIS</span></span>
<span data-ttu-id="e0808-103">A privát hivatkozás szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="e0808-103">Updates a private link service.</span></span>

## <span data-ttu-id="e0808-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0808-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0808-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0808-105">DESCRIPTION</span></span>
<span data-ttu-id="e0808-106">A **set-AzPrivateLinkService** parancsmag frissíti a privát hivatkozás szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e0808-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="e0808-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0808-107">EXAMPLES</span></span>

### <span data-ttu-id="e0808-108">1: privát hivatkozás szolgáltatás létrehozása és frissítése</span><span class="sxs-lookup"><span data-stu-id="e0808-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="e0808-109">Ebben a példában a mypls nevű privát hivatkozás szolgáltatás jön létre.</span><span class="sxs-lookup"><span data-stu-id="e0808-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="e0808-110">Ezután a memóriabeli ipConfiguratiuon objektumból cseréli a ipConfigurations.</span><span class="sxs-lookup"><span data-stu-id="e0808-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="e0808-111">A rendszer a Set-AzPrivateLinkService parancsmagot használja a szolgáltatás oldalán a módosított privát kapcsolat szolgáltatás állapotának megírásához.</span><span class="sxs-lookup"><span data-stu-id="e0808-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="e0808-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0808-112">PARAMETERS</span></span>

### <span data-ttu-id="e0808-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0808-113">-AsJob</span></span>
<span data-ttu-id="e0808-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e0808-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0808-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0808-115">-DefaultProfile</span></span>
<span data-ttu-id="e0808-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0808-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0808-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e0808-117">-PrivateLinkService</span></span>
<span data-ttu-id="e0808-118">Megadja azt az államot, amely azt az államot képviseli, amelyhez a privát kapcsolat szolgáltatást be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="e0808-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0808-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0808-119">CommonParameters</span></span>
<span data-ttu-id="e0808-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0808-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0808-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0808-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0808-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0808-122">INPUTS</span></span>

### <span data-ttu-id="e0808-123">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e0808-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e0808-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0808-124">OUTPUTS</span></span>

### <span data-ttu-id="e0808-125">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e0808-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e0808-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0808-126">NOTES</span></span>

## <span data-ttu-id="e0808-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0808-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0808-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e0808-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="e0808-129">Új – AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e0808-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="e0808-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e0808-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


