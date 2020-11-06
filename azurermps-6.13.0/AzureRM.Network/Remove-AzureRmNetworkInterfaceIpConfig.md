---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: c912d32c39380ee3d653fa228632a4d01f0e3049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495884"
---
# <span data-ttu-id="bef6c-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bef6c-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="bef6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bef6c-102">SYNOPSIS</span></span>
<span data-ttu-id="bef6c-103">Hálózati kapcsolat IP-konfigurációjának eltávolítása hálózati kapcsolatból.</span><span class="sxs-lookup"><span data-stu-id="bef6c-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bef6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bef6c-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bef6c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bef6c-105">DESCRIPTION</span></span>
<span data-ttu-id="bef6c-106">A **Remove-AzureRmNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati felületről távolítja el.</span><span class="sxs-lookup"><span data-stu-id="bef6c-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="bef6c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bef6c-107">EXAMPLES</span></span>

### <span data-ttu-id="bef6c-108">1: IP-konfiguráció törlése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="bef6c-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="bef6c-109">Az első parancs a mynic nevű hálózati felületet kapja, és a változó $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="bef6c-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="bef6c-110">A második parancs eltávolítja az e hálózati csatolóval társított IPConfig-1 nevű IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="bef6c-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="bef6c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bef6c-111">PARAMETERS</span></span>

### <span data-ttu-id="bef6c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef6c-112">-DefaultProfile</span></span>
<span data-ttu-id="bef6c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bef6c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bef6c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bef6c-114">-Name</span></span>
<span data-ttu-id="bef6c-115">Annak a hálózati kapcsolatnak az IP-konfigurációjának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="bef6c-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="bef6c-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bef6c-116">-NetworkInterface</span></span>
<span data-ttu-id="bef6c-117">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bef6c-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="bef6c-118">Ez az objektum az eltávolítandó hálózati kapcsolat IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bef6c-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="bef6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef6c-119">CommonParameters</span></span>
<span data-ttu-id="bef6c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bef6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef6c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef6c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef6c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bef6c-122">INPUTS</span></span>

### <span data-ttu-id="bef6c-123">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bef6c-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="bef6c-124">Paraméterek: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bef6c-124">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="bef6c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bef6c-125">OUTPUTS</span></span>

### <span data-ttu-id="bef6c-126">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bef6c-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="bef6c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bef6c-127">NOTES</span></span>
* <span data-ttu-id="bef6c-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="bef6c-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bef6c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bef6c-129">RELATED LINKS</span></span>

[<span data-ttu-id="bef6c-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bef6c-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bef6c-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bef6c-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bef6c-132">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bef6c-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bef6c-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bef6c-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


