---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: d532bbee77d028afb4af441dd511deafa6ebc016
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837099"
---
# <span data-ttu-id="dd457-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd457-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="dd457-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd457-102">SYNOPSIS</span></span>
<span data-ttu-id="dd457-103">Hálózati kapcsolat IP-konfigurációjának eltávolítása hálózati kapcsolatból.</span><span class="sxs-lookup"><span data-stu-id="dd457-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="dd457-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd457-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd457-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd457-105">DESCRIPTION</span></span>
<span data-ttu-id="dd457-106">A **Remove-AzNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati felületről távolítja el.</span><span class="sxs-lookup"><span data-stu-id="dd457-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="dd457-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd457-107">EXAMPLES</span></span>

### <span data-ttu-id="dd457-108">1: IP-konfiguráció törlése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="dd457-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="dd457-109">Az első parancs a mynic nevű hálózati felületet kapja, és a változó $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="dd457-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="dd457-110">A második parancs eltávolítja az e hálózati csatolóval társított IPConfig-1 nevű IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dd457-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="dd457-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd457-111">PARAMETERS</span></span>

### <span data-ttu-id="dd457-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd457-112">-DefaultProfile</span></span>
<span data-ttu-id="dd457-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd457-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd457-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd457-114">-Name</span></span>
<span data-ttu-id="dd457-115">Annak a hálózati kapcsolatnak az IP-konfigurációjának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="dd457-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="dd457-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd457-116">-NetworkInterface</span></span>
<span data-ttu-id="dd457-117">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="dd457-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="dd457-118">Ez az objektum az eltávolítandó hálózati kapcsolat IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dd457-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd457-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd457-119">CommonParameters</span></span>
<span data-ttu-id="dd457-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd457-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd457-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd457-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd457-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd457-122">INPUTS</span></span>

### <span data-ttu-id="dd457-123">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd457-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="dd457-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd457-124">OUTPUTS</span></span>

### <span data-ttu-id="dd457-125">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd457-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="dd457-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd457-126">NOTES</span></span>
* <span data-ttu-id="dd457-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="dd457-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dd457-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd457-128">RELATED LINKS</span></span>

[<span data-ttu-id="dd457-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd457-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dd457-130">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd457-130">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dd457-131">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd457-131">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dd457-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd457-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


