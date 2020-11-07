---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 24cbdaebc21456268d050b5c3a56ec9fc443fedf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670363"
---
# <span data-ttu-id="ddaa7-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddaa7-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="ddaa7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddaa7-102">SYNOPSIS</span></span>
<span data-ttu-id="ddaa7-103">Tároló NIC-konfiguráció IP-konfigurációs objektumának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="ddaa7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddaa7-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddaa7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddaa7-105">DESCRIPTION</span></span>
<span data-ttu-id="ddaa7-106">A **New-AzContainerNicConfigIpConfig** parancsmag létrehoz egy új tároló hálózati illesztőfelület-konfiguráció IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="ddaa7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ddaa7-107">EXAMPLES</span></span>

### <span data-ttu-id="ddaa7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ddaa7-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="ddaa7-109">Az első két parancs a vnet és az alhálózatokat hozza létre és inicializálja.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="ddaa7-110">A harmadik parancs létrehoz egy tároló NIC IP-konfigurációs profilt, amelyre a létrehozott alhálózat hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="ddaa7-111">A negyedik parancs létrehoz egy tároló hálózati illesztőfelület-konfigurációt, amely az előző parancsban létrehozott IP-konfigurációs profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="ddaa7-112">Végül az ötödik parancs létrehoz egy hálózati profilt, amelyet az $containerNicConfig-ban tárolt tároló hálózati illesztőfelület-konfigurációval inicializált.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="ddaa7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddaa7-113">PARAMETERS</span></span>

### <span data-ttu-id="ddaa7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddaa7-114">-DefaultProfile</span></span>
<span data-ttu-id="ddaa7-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddaa7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddaa7-116">-Name</span></span>
<span data-ttu-id="ddaa7-117">A Container hálózati felületének konfigurációja IP-konfigurációs profiljának neve.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="ddaa7-118">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="ddaa7-118">-Subnet</span></span>
<span data-ttu-id="ddaa7-119">Alhálózati</span><span class="sxs-lookup"><span data-stu-id="ddaa7-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddaa7-120">– NetI</span><span class="sxs-lookup"><span data-stu-id="ddaa7-120">-SubnetId</span></span>
<span data-ttu-id="ddaa7-121">Beadott</span><span class="sxs-lookup"><span data-stu-id="ddaa7-121">SubnetId</span></span>

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

### <span data-ttu-id="ddaa7-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ddaa7-122">-Confirm</span></span>
<span data-ttu-id="ddaa7-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddaa7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddaa7-124">-WhatIf</span></span>
<span data-ttu-id="ddaa7-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddaa7-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddaa7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddaa7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddaa7-127">CommonParameters</span></span>
<span data-ttu-id="ddaa7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddaa7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddaa7-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddaa7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddaa7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddaa7-130">INPUTS</span></span>

### <span data-ttu-id="ddaa7-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="ddaa7-131">None</span></span>

## <span data-ttu-id="ddaa7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddaa7-132">OUTPUTS</span></span>

### <span data-ttu-id="ddaa7-133">Microsoft. Azure. commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddaa7-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="ddaa7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddaa7-134">NOTES</span></span>

## <span data-ttu-id="ddaa7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddaa7-135">RELATED LINKS</span></span>

[<span data-ttu-id="ddaa7-136">Új – AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ddaa7-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
