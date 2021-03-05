---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: fc0e3ad0bcc86a0ad49450393a79c6c60540ba23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001061"
---
# <span data-ttu-id="ef536-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ef536-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="ef536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef536-102">SYNOPSIS</span></span>
<span data-ttu-id="ef536-103">Egy privát hivatkozásszolgáltatás frissítése.</span><span class="sxs-lookup"><span data-stu-id="ef536-103">Updates a private link service.</span></span>

## <span data-ttu-id="ef536-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef536-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef536-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef536-105">DESCRIPTION</span></span>
<span data-ttu-id="ef536-106">A **Set-AzPrivateLinkService** parancsmag frissíti a privát hivatkozásszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="ef536-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="ef536-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef536-107">EXAMPLES</span></span>

### <span data-ttu-id="ef536-108">1: Privát hivatkozásszolgáltatás létrehozása és frissítése</span><span class="sxs-lookup"><span data-stu-id="ef536-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="ef536-109">Ez a példa létrehoz egy mypls nevű privát hivatkozásszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="ef536-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="ef536-110">Ezután lecseréli az ipConfigurációkat a memóriában beállított ipConfiguratiuon objektumból.</span><span class="sxs-lookup"><span data-stu-id="ef536-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="ef536-111">A Set-AzPrivateLinkService ezt követően a szolgáltatásoldalon megírja a módosított privát hivatkozásszolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="ef536-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="ef536-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef536-112">PARAMETERS</span></span>

### <span data-ttu-id="ef536-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef536-113">-AsJob</span></span>
<span data-ttu-id="ef536-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ef536-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef536-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef536-115">-DefaultProfile</span></span>
<span data-ttu-id="ef536-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef536-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef536-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ef536-117">-PrivateLinkService</span></span>
<span data-ttu-id="ef536-118">Egy privát csatolási szolgáltatásobjektumot ad meg, amely azt az állapotot képviseli, amelyben a privát csatolási szolgáltatást be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="ef536-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="ef536-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef536-119">CommonParameters</span></span>
<span data-ttu-id="ef536-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef536-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef536-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef536-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef536-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef536-122">INPUTS</span></span>

### <span data-ttu-id="ef536-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ef536-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ef536-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef536-124">OUTPUTS</span></span>

### <span data-ttu-id="ef536-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ef536-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ef536-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef536-126">NOTES</span></span>

## <span data-ttu-id="ef536-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef536-127">RELATED LINKS</span></span>

[<span data-ttu-id="ef536-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ef536-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="ef536-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ef536-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="ef536-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ef536-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


