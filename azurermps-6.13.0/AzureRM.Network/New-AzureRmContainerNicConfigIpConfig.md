---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498320"
---
# <span data-ttu-id="d3dbf-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d3dbf-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="d3dbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="d3dbf-103">Tároló NIC-konfiguráció IP-konfigurációs objektumának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3dbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3dbf-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3dbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="d3dbf-106">A **New-AzureRmNetworkProfileContainerNicConfigIpConfig** parancsmag létrehoz egy új tároló hálózati illesztőfelület-konfiguráció IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="d3dbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d3dbf-107">EXAMPLES</span></span>

### <span data-ttu-id="d3dbf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3dbf-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="d3dbf-109">Az első két parancs a vnet és az alhálózatokat hozza létre és inicializálja.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="d3dbf-110">A harmadik parancs létrehoz egy tároló NIC IP-konfigurációs profilt, amelyre a létrehozott alhálózat hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="d3dbf-111">A negyedik parancs létrehoz egy tároló hálózati illesztőfelület-konfigurációt, amely az előző parancsban létrehozott IP-konfigurációs profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="d3dbf-112">Végül az ötödik parancs létrehoz egy hálózati profilt, amelyet az $containerNicConfig-ban tárolt tároló hálózati illesztőfelület-konfigurációval inicializált.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="d3dbf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3dbf-113">PARAMETERS</span></span>

### <span data-ttu-id="d3dbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3dbf-114">-DefaultProfile</span></span>
<span data-ttu-id="d3dbf-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3dbf-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3dbf-116">-Name</span></span>
<span data-ttu-id="d3dbf-117">A Container hálózati felületének konfigurációja IP-konfigurációs profiljának neve.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="d3dbf-118">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="d3dbf-118">-Subnet</span></span>
<span data-ttu-id="d3dbf-119">Alhálózati</span><span class="sxs-lookup"><span data-stu-id="d3dbf-119">Subnet</span></span>

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

### <span data-ttu-id="d3dbf-120">– NetI</span><span class="sxs-lookup"><span data-stu-id="d3dbf-120">-SubnetId</span></span>
<span data-ttu-id="d3dbf-121">Beadott</span><span class="sxs-lookup"><span data-stu-id="d3dbf-121">SubnetId</span></span>

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

### <span data-ttu-id="d3dbf-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3dbf-122">-Confirm</span></span>
<span data-ttu-id="d3dbf-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3dbf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3dbf-124">-WhatIf</span></span>
<span data-ttu-id="d3dbf-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3dbf-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3dbf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3dbf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3dbf-127">CommonParameters</span></span>
<span data-ttu-id="d3dbf-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3dbf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3dbf-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3dbf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3dbf-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3dbf-130">INPUTS</span></span>

### <span data-ttu-id="d3dbf-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3dbf-131">None</span></span>

## <span data-ttu-id="d3dbf-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3dbf-132">OUTPUTS</span></span>

### <span data-ttu-id="d3dbf-133">Microsoft. Azure. commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3dbf-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="d3dbf-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3dbf-134">NOTES</span></span>

## <span data-ttu-id="d3dbf-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3dbf-135">RELATED LINKS</span></span>
