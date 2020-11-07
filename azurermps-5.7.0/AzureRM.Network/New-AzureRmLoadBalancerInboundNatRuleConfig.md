---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 0b974d1d79be82f3c16f1052abe0eecc7fa9ba30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678968"
---
# <span data-ttu-id="57672-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57672-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="57672-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57672-102">SYNOPSIS</span></span>
<span data-ttu-id="57672-103">Bejövő hálózati címfordítási szabály konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="57672-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57672-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57672-104">SYNTAX</span></span>

### <span data-ttu-id="57672-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="57672-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57672-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="57672-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57672-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="57672-107">DESCRIPTION</span></span>
<span data-ttu-id="57672-108">A **New-AzureRmLoadBalancerInboundNatRuleConfig** parancsmag beérkező hálózati címfordítási (NAT) szabály-konfigurációt hoz létre az Azure terheléselosztó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="57672-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="57672-109">Példák</span><span class="sxs-lookup"><span data-stu-id="57672-109">EXAMPLES</span></span>

### <span data-ttu-id="57672-110">1. példa: bejövő hálózati címfordítási szabály konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="57672-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="57672-111">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="57672-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="57672-112">A második parancs létrehozza a FrontendIpConfig01 nevű előtér-IP-konfigurációt a $publicip nyilvános IP-címével, majd a $frontend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="57672-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="57672-113">A harmadik parancs a MyInboundNatRule nevű bejövő NAT-szabály konfigurációját a $frontend előtér objektumával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="57672-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="57672-114">A TCP protokoll meg van adva, és az előtér-végpont a 3389, ugyanaz, mint a backend port ebben az esetben.</span><span class="sxs-lookup"><span data-stu-id="57672-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="57672-115">A *FrontendIpConfiguration* , az *procotol* , a *FrontendPort* és a *BACKENDPORT* paraméterek mind szükségesek a bejövő címfordítási szabályok konfigurációjának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="57672-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="57672-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57672-116">PARAMETERS</span></span>

### <span data-ttu-id="57672-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="57672-117">-BackendPort</span></span>
<span data-ttu-id="57672-118">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="57672-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57672-119">-DefaultProfile</span></span>
<span data-ttu-id="57672-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57672-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="57672-121">-EnableFloatingIP</span></span>
<span data-ttu-id="57672-122">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="57672-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="57672-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="57672-124">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="57672-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="57672-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="57672-126">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="57672-126">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="57672-127">-FrontendPort</span></span>
<span data-ttu-id="57672-128">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="57672-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="57672-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="57672-130">Azt adja meg, hogy hány percen belül maradjon a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="57672-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57672-131">-Name</span></span>
<span data-ttu-id="57672-132">A parancsmag által létrehozott szabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57672-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="57672-133">-Protocol</span></span>
<span data-ttu-id="57672-134">Egy protokollt ad meg.</span><span class="sxs-lookup"><span data-stu-id="57672-134">Specifies a protocol.</span></span>
<span data-ttu-id="57672-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="57672-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57672-136">TCP</span><span class="sxs-lookup"><span data-stu-id="57672-136">Tcp</span></span>
- <span data-ttu-id="57672-137">UDP</span><span class="sxs-lookup"><span data-stu-id="57672-137">Udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57672-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57672-138">CommonParameters</span></span>
<span data-ttu-id="57672-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57672-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57672-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57672-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57672-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57672-141">INPUTS</span></span>

### <span data-ttu-id="57672-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="57672-142">None</span></span>
<span data-ttu-id="57672-143">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="57672-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57672-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57672-144">OUTPUTS</span></span>

### <span data-ttu-id="57672-145">Microsoft. Azure. commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="57672-145">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="57672-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57672-146">NOTES</span></span>

## <span data-ttu-id="57672-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57672-147">RELATED LINKS</span></span>

[<span data-ttu-id="57672-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57672-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="57672-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57672-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="57672-150">Új – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="57672-150">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="57672-151">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="57672-151">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="57672-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57672-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="57672-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57672-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


