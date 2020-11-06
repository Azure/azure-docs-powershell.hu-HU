---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 2245fa10d160fc0f6b085a039214f9bcd72404a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493658"
---
# <span data-ttu-id="bd52f-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bd52f-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="bd52f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd52f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd52f-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd52f-103">SYNTAX</span></span>

### <span data-ttu-id="bd52f-104">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd52f-104">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd52f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd52f-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd52f-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd52f-106">DESCRIPTION</span></span>

## <span data-ttu-id="bd52f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bd52f-107">EXAMPLES</span></span>

### <span data-ttu-id="bd52f-108">1: Hozzáadás</span><span class="sxs-lookup"><span data-stu-id="bd52f-108">1: Add</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="bd52f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd52f-109">PARAMETERS</span></span>

### <span data-ttu-id="bd52f-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bd52f-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd52f-111">-DefaultProfile</span></span>
<span data-ttu-id="bd52f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd52f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd52f-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bd52f-113">-EnableFloatingIP</span></span>
<span data-ttu-id="bd52f-114">Beállítja a virtuális gép végpontját az SQL-AlwaysOn elérhetőségi csoportjának beállításához szükséges lebegő IP-kapacitáshoz.</span><span class="sxs-lookup"><span data-stu-id="bd52f-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="bd52f-115">Ez a beállítás akkor szükséges, ha az SQL Server-AlwaysOn elérhetőségi csoportjait használja.</span><span class="sxs-lookup"><span data-stu-id="bd52f-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="bd52f-116">A végpont létrehozása után ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="bd52f-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="bd52f-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="bd52f-117">-EnableTcpReset</span></span>
<span data-ttu-id="bd52f-118">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="bd52f-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="bd52f-119">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="bd52f-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="bd52f-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd52f-120">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bd52f-121">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="bd52f-122">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="bd52f-123">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bd52f-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bd52f-125">A TCP Idle-kapcsolat időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="bd52f-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="bd52f-126">Az érték 4 és 30 perc között állítható be.</span><span class="sxs-lookup"><span data-stu-id="bd52f-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="bd52f-127">Az alapértelmezett érték 4 perc.</span><span class="sxs-lookup"><span data-stu-id="bd52f-127">The default value is 4 minutes.</span></span> <span data-ttu-id="bd52f-128">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="bd52f-128">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-129">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd52f-129">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd52f-130">-Name</span></span>
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

### <span data-ttu-id="bd52f-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="bd52f-131">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd52f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd52f-132">-Confirm</span></span>
<span data-ttu-id="bd52f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd52f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd52f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd52f-134">-WhatIf</span></span>
<span data-ttu-id="bd52f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd52f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd52f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd52f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd52f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd52f-137">CommonParameters</span></span>
<span data-ttu-id="bd52f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd52f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd52f-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd52f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd52f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd52f-140">INPUTS</span></span>

### <span data-ttu-id="bd52f-141">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd52f-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="bd52f-142">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bd52f-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="bd52f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd52f-143">OUTPUTS</span></span>

### <span data-ttu-id="bd52f-144">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd52f-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bd52f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd52f-145">NOTES</span></span>

## <span data-ttu-id="bd52f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd52f-146">RELATED LINKS</span></span>
