---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172917"
---
# <span data-ttu-id="3b58c-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b58c-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="3b58c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b58c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b58c-103">Hálózati kapcsolat IP-konfigurációjának eltávolítása hálózati kapcsolatból.</span><span class="sxs-lookup"><span data-stu-id="3b58c-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="3b58c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b58c-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b58c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b58c-105">DESCRIPTION</span></span>
<span data-ttu-id="3b58c-106">A **Remove-AzNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati felületről távolítja el.</span><span class="sxs-lookup"><span data-stu-id="3b58c-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="3b58c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b58c-107">EXAMPLES</span></span>

### <span data-ttu-id="3b58c-108">Példa 1: IP-konfiguráció törlése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="3b58c-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="3b58c-109">Az első parancs a mynic nevű hálózati felületet kapja, és a változó $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="3b58c-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="3b58c-110">A második parancs eltávolítja az e hálózati csatolóval társított IPConfig-1 nevű IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="3b58c-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="3b58c-111">A harmadik parancs beállítja a hálózati felületen végzett módosításokat.</span><span class="sxs-lookup"><span data-stu-id="3b58c-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="3b58c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b58c-112">PARAMETERS</span></span>

### <span data-ttu-id="3b58c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b58c-113">-DefaultProfile</span></span>
<span data-ttu-id="3b58c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b58c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b58c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b58c-115">-Name</span></span>
<span data-ttu-id="3b58c-116">Annak a hálózati kapcsolatnak az IP-konfigurációjának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="3b58c-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="3b58c-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3b58c-117">-NetworkInterface</span></span>
<span data-ttu-id="3b58c-118">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3b58c-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="3b58c-119">Ez az objektum az eltávolítandó hálózati kapcsolat IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3b58c-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="3b58c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b58c-120">CommonParameters</span></span>
<span data-ttu-id="3b58c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b58c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b58c-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b58c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b58c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b58c-123">INPUTS</span></span>

### <span data-ttu-id="3b58c-124">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3b58c-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="3b58c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b58c-125">OUTPUTS</span></span>

### <span data-ttu-id="3b58c-126">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3b58c-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="3b58c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b58c-127">NOTES</span></span>
* <span data-ttu-id="3b58c-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="3b58c-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3b58c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b58c-129">RELATED LINKS</span></span>

[<span data-ttu-id="3b58c-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b58c-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3b58c-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b58c-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3b58c-132">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b58c-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3b58c-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b58c-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


