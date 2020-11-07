---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: c9ffd5b3a61dab57859f8c099950ddca0f47822c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848126"
---
# <span data-ttu-id="44ea4-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="44ea4-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="44ea4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="44ea4-103">Hálózati kapcsolat IP-konfigurációjának eltávolítása hálózati kapcsolatból.</span><span class="sxs-lookup"><span data-stu-id="44ea4-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44ea4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44ea4-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ea4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="44ea4-106">A **Remove-AzureRmNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati felületről távolítja el.</span><span class="sxs-lookup"><span data-stu-id="44ea4-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="44ea4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44ea4-107">EXAMPLES</span></span>

### <span data-ttu-id="44ea4-108">1: IP-konfiguráció törlése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="44ea4-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="44ea4-109">Az első parancs a mynic nevű hálózati felületet kapja, és a változó $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="44ea4-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="44ea4-110">A második parancs eltávolítja az e hálózati csatolóval társított IPConfig-1 nevű IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="44ea4-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="44ea4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44ea4-111">PARAMETERS</span></span>

### <span data-ttu-id="44ea4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ea4-112">-DefaultProfile</span></span>
<span data-ttu-id="44ea4-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44ea4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44ea4-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44ea4-114">-Name</span></span>
<span data-ttu-id="44ea4-115">Annak a hálózati kapcsolatnak az IP-konfigurációjának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="44ea4-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="44ea4-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44ea4-116">-NetworkInterface</span></span>
<span data-ttu-id="44ea4-117">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="44ea4-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="44ea4-118">Ez az objektum az eltávolítandó hálózati kapcsolat IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="44ea4-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44ea4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ea4-119">CommonParameters</span></span>
<span data-ttu-id="44ea4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44ea4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ea4-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ea4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ea4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44ea4-122">INPUTS</span></span>

### <span data-ttu-id="44ea4-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44ea4-123">PSNetworkInterface</span></span>
<span data-ttu-id="44ea4-124">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="44ea4-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="44ea4-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44ea4-125">OUTPUTS</span></span>

### <span data-ttu-id="44ea4-126">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44ea4-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="44ea4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44ea4-127">NOTES</span></span>
* <span data-ttu-id="44ea4-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="44ea4-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="44ea4-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44ea4-129">RELATED LINKS</span></span>

[<span data-ttu-id="44ea4-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="44ea4-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="44ea4-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="44ea4-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="44ea4-132">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="44ea4-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="44ea4-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="44ea4-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


