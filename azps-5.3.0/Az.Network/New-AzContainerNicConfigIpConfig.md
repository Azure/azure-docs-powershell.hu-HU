---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379216"
---
# <span data-ttu-id="7270c-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7270c-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="7270c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7270c-102">SYNOPSIS</span></span>
<span data-ttu-id="7270c-103">Létrehoz egy container nic configuration ip configuration object.</span><span class="sxs-lookup"><span data-stu-id="7270c-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="7270c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7270c-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7270c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7270c-105">DESCRIPTION</span></span>
<span data-ttu-id="7270c-106">A **New-AzContainerNicConfigIpConfig** parancsmag létrehoz egy új tárolóhálózati felület konfigurációjának IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7270c-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="7270c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7270c-107">EXAMPLES</span></span>

### <span data-ttu-id="7270c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7270c-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="7270c-109">Az első két parancs létrehoz és inicializál egy vnetet és egy alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="7270c-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="7270c-110">A harmadik parancs létrehoz egy tároló nic ip konfigurációs profilt, amely hivatkozik a létrehozott alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="7270c-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="7270c-111">A negyedik parancs létrehoz egy tárolóhálózati felületet, amely az előző parancsban létrehozott IP-konfigurációs profilt használja.</span><span class="sxs-lookup"><span data-stu-id="7270c-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="7270c-112">Végül az ötödik parancs létrehoz egy olyan hálózati profilt, amely inicializálva van a tárolóhálózati felület $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="7270c-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="7270c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7270c-113">PARAMETERS</span></span>

### <span data-ttu-id="7270c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7270c-114">-DefaultProfile</span></span>
<span data-ttu-id="7270c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7270c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7270c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7270c-116">-Name</span></span>
<span data-ttu-id="7270c-117">A tárolóhálózati kapcsolat konfigurációs IP-konfigurációs profiljának neve.</span><span class="sxs-lookup"><span data-stu-id="7270c-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="7270c-118">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="7270c-118">-Subnet</span></span>
<span data-ttu-id="7270c-119">Alhálózat</span><span class="sxs-lookup"><span data-stu-id="7270c-119">Subnet</span></span>

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

### <span data-ttu-id="7270c-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7270c-120">-SubnetId</span></span>
<span data-ttu-id="7270c-121">Alhálózatazonosító</span><span class="sxs-lookup"><span data-stu-id="7270c-121">SubnetId</span></span>

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

### <span data-ttu-id="7270c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7270c-122">-Confirm</span></span>
<span data-ttu-id="7270c-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7270c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7270c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7270c-124">-WhatIf</span></span>
<span data-ttu-id="7270c-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7270c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7270c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7270c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7270c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7270c-127">CommonParameters</span></span>
<span data-ttu-id="7270c-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7270c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7270c-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7270c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7270c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7270c-130">INPUTS</span></span>

### <span data-ttu-id="7270c-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="7270c-131">None</span></span>

## <span data-ttu-id="7270c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7270c-132">OUTPUTS</span></span>

### <span data-ttu-id="7270c-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7270c-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="7270c-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7270c-134">NOTES</span></span>

## <span data-ttu-id="7270c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7270c-135">RELATED LINKS</span></span>

[<span data-ttu-id="7270c-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7270c-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
