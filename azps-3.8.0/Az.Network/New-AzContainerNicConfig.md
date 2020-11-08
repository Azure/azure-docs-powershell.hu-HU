---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 75f05c76b76f37e936798766d9288ace38d1397f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014758"
---
# <span data-ttu-id="fc5ad-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fc5ad-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="fc5ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5ad-103">Új tároló hálózati csatoló konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="fc5ad-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="fc5ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc5ad-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc5ad-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5ad-106">A **New-AzContainerNicConfig** parancsmag létrehoz egy új tároló hálózati adapter-konfiguráció objektumát.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="fc5ad-107">Ez az objektum határozza meg, hogy a Container hálózati felülete milyen jellemzőit hozza létre a szülő hálózati profilra hivatkozva.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="fc5ad-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fc5ad-108">EXAMPLES</span></span>

### <span data-ttu-id="fc5ad-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc5ad-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="fc5ad-110">Az első parancs létrehoz egy üres tároló hálózati illesztőfelület-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="fc5ad-111">A második létrehoz egy új hálózati profilt, amely a korábban létrehozott tároló hálózati felületének konfigurációját az New-NetworkProfile parancsmag argumentumaként adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="fc5ad-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc5ad-112">PARAMETERS</span></span>

### <span data-ttu-id="fc5ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5ad-113">-DefaultProfile</span></span>
<span data-ttu-id="fc5ad-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5ad-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc5ad-115">-IpConfiguration</span></span>
<span data-ttu-id="fc5ad-116">Az IP-konfigurációs profilok gyűjteménye, amely meghatározza, hogy mely IP-konfigurációkat hozza létre a rendszer, ha a tároló hálózati felületének konfigurációja</span><span class="sxs-lookup"><span data-stu-id="fc5ad-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5ad-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc5ad-117">-Name</span></span>
<span data-ttu-id="fc5ad-118">A tároló hálózati felületének konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="fc5ad-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc5ad-119">-Confirm</span></span>
<span data-ttu-id="fc5ad-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5ad-121">-WhatIf</span></span>
<span data-ttu-id="fc5ad-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5ad-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc5ad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5ad-124">CommonParameters</span></span>
<span data-ttu-id="fc5ad-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc5ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5ad-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5ad-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5ad-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc5ad-127">INPUTS</span></span>

### <span data-ttu-id="fc5ad-128">Microsoft. Azure. commands. Network. models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="fc5ad-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="fc5ad-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc5ad-129">OUTPUTS</span></span>

### <span data-ttu-id="fc5ad-130">Microsoft. Azure. commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc5ad-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="fc5ad-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc5ad-131">NOTES</span></span>

## <span data-ttu-id="fc5ad-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc5ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc5ad-133">Új – AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc5ad-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
