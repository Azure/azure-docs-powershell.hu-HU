---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 52aad9586840875cf63a27a8f27ff7296d080bd7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841330"
---
# <span data-ttu-id="47d1f-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47d1f-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="47d1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="47d1f-103">Bejövő hálózati címfordítási szabály konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="47d1f-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="47d1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47d1f-104">SYNTAX</span></span>

### <span data-ttu-id="47d1f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47d1f-105">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d1f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="47d1f-106">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47d1f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47d1f-107">DESCRIPTION</span></span>
<span data-ttu-id="47d1f-108">A **New-AzLoadBalancerInboundNatRuleConfig** parancsmag beérkező hálózati címfordítási (NAT) szabály-konfigurációt hoz létre az Azure terheléselosztó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="47d1f-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="47d1f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="47d1f-109">EXAMPLES</span></span>

### <span data-ttu-id="47d1f-110">1. példa: bejövő hálózati címfordítási szabály konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="47d1f-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="47d1f-111">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="47d1f-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="47d1f-112">A második parancs létrehozza a FrontendIpConfig01 nevű előtér-IP-konfigurációt a $publicip nyilvános IP-címével, majd a $frontend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="47d1f-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="47d1f-113">A harmadik parancs a MyInboundNatRule nevű bejövő NAT-szabály konfigurációját a $frontend előtér objektumával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="47d1f-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="47d1f-114">A TCP protokoll meg van adva, és az előtér-végpont a 3389, ugyanaz, mint a backend port ebben az esetben.</span><span class="sxs-lookup"><span data-stu-id="47d1f-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="47d1f-115">A *FrontendIpConfiguration* , az *procotol* , a *FrontendPort* és a *BACKENDPORT* paraméterek mind szükségesek a bejövő címfordítási szabályok konfigurációjának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="47d1f-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="47d1f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47d1f-116">PARAMETERS</span></span>

### <span data-ttu-id="47d1f-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="47d1f-117">-BackendPort</span></span>
<span data-ttu-id="47d1f-118">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="47d1f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d1f-119">-DefaultProfile</span></span>
<span data-ttu-id="47d1f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47d1f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47d1f-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="47d1f-121">-EnableFloatingIP</span></span>
<span data-ttu-id="47d1f-122">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="47d1f-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="47d1f-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="47d1f-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="47d1f-124">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="47d1f-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="47d1f-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="47d1f-126">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-126">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="47d1f-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="47d1f-127">-FrontendPort</span></span>
<span data-ttu-id="47d1f-128">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="47d1f-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="47d1f-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="47d1f-130">Azt adja meg, hogy hány percen belül maradjon a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="47d1f-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="47d1f-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47d1f-131">-Name</span></span>
<span data-ttu-id="47d1f-132">A parancsmag által létrehozott szabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="47d1f-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="47d1f-133">-Protocol</span></span>
<span data-ttu-id="47d1f-134">Egy protokollt ad meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-134">Specifies a protocol.</span></span>
<span data-ttu-id="47d1f-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="47d1f-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47d1f-136">TCP</span><span class="sxs-lookup"><span data-stu-id="47d1f-136">Tcp</span></span>
- <span data-ttu-id="47d1f-137">UDP</span><span class="sxs-lookup"><span data-stu-id="47d1f-137">Udp</span></span>

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

### <span data-ttu-id="47d1f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d1f-138">CommonParameters</span></span>
<span data-ttu-id="47d1f-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47d1f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d1f-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d1f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d1f-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d1f-141">INPUTS</span></span>

## <span data-ttu-id="47d1f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d1f-142">OUTPUTS</span></span>

### <span data-ttu-id="47d1f-143">Microsoft. Azure. commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="47d1f-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="47d1f-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47d1f-144">NOTES</span></span>

## <span data-ttu-id="47d1f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47d1f-145">RELATED LINKS</span></span>

[<span data-ttu-id="47d1f-146">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47d1f-146">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="47d1f-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47d1f-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="47d1f-148">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47d1f-148">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="47d1f-149">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="47d1f-149">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="47d1f-150">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47d1f-150">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="47d1f-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47d1f-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


