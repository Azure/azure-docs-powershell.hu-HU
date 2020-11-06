---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 004180f2369616654741df960a56a9f9c5bb6047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494821"
---
# <span data-ttu-id="39cdf-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39cdf-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="39cdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="39cdf-103">Bejövő hálózati címfordítási szabály konfigurációjának beállítása terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="39cdf-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39cdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39cdf-104">SYNTAX</span></span>

### <span data-ttu-id="39cdf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39cdf-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39cdf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="39cdf-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39cdf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="39cdf-107">DESCRIPTION</span></span>
<span data-ttu-id="39cdf-108">A **set-AzureRmLoadBalancerInboundNatRuleConfig** parancsmag egy beérkező hálózati címfordítási (NAT) szabály-konfigurációt állít be egy Azure-terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="39cdf-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="39cdf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39cdf-109">EXAMPLES</span></span>

### <span data-ttu-id="39cdf-110">Példa 1: a bejövő CÍMFORDÍTÁSi szabály konfigurációjának módosítása a terheléselosztó eszközön</span><span class="sxs-lookup"><span data-stu-id="39cdf-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="39cdf-111">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="39cdf-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="39cdf-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzureRmLoadBalancerInboundNatRuleConfig-hoz, ami beérkező hálózati címfordítási szabály konfigurációját adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="39cdf-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="39cdf-113">A harmadik parancs átadja a kiegyenlítőt a **set-AzureRmLoadBalancerInboundNatRuleConfig** , amely menti és FRISSÍTI a NAT-szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="39cdf-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="39cdf-114">Fontos tudni, hogy a szabály konfigurációja a lebegő IP engedélyezése nélkül volt beállítva, amelyet az előző parancs engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="39cdf-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="39cdf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39cdf-115">PARAMETERS</span></span>

### <span data-ttu-id="39cdf-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="39cdf-116">-BackendPort</span></span>
<span data-ttu-id="39cdf-117">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="39cdf-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="39cdf-118">-EnableFloatingIP</span></span>
<span data-ttu-id="39cdf-119">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="39cdf-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="39cdf-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39cdf-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="39cdf-121">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="39cdf-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39cdf-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="39cdf-123">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="39cdf-123">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="39cdf-124">-FrontendPort</span></span>
<span data-ttu-id="39cdf-125">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="39cdf-125">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="39cdf-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="39cdf-127">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="39cdf-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39cdf-128">-LoadBalancer</span></span>
<span data-ttu-id="39cdf-129">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="39cdf-129">Specifies a load balancer.</span></span>
<span data-ttu-id="39cdf-130">Ez a parancsmag bejelöli a hálózati címfordítási szabály konfigurációját a paraméter által megadott terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="39cdf-130">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39cdf-131">-Name</span></span>
<span data-ttu-id="39cdf-132">A beérkező NAT-szabályok konfigurációjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39cdf-132">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="39cdf-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="39cdf-133">-Protocol</span></span>
<span data-ttu-id="39cdf-134">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjának megfelelő protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="39cdf-134">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="39cdf-135">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="39cdf-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39cdf-136">-DefaultProfile</span></span>
<span data-ttu-id="39cdf-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39cdf-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cdf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39cdf-138">CommonParameters</span></span>
<span data-ttu-id="39cdf-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39cdf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39cdf-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39cdf-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39cdf-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39cdf-141">INPUTS</span></span>

### <span data-ttu-id="39cdf-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39cdf-142">PSLoadBalancer</span></span>
<span data-ttu-id="39cdf-143">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="39cdf-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="39cdf-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39cdf-144">OUTPUTS</span></span>

### <span data-ttu-id="39cdf-145">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39cdf-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="39cdf-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39cdf-146">NOTES</span></span>

## <span data-ttu-id="39cdf-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39cdf-147">RELATED LINKS</span></span>

[<span data-ttu-id="39cdf-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39cdf-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="39cdf-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39cdf-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="39cdf-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39cdf-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="39cdf-151">Új – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39cdf-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="39cdf-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39cdf-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


