---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8afc90c8709869a9acf3464c4ad39bdbc2b3ab5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492460"
---
# <span data-ttu-id="6695f-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6695f-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="6695f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6695f-102">SYNOPSIS</span></span>
<span data-ttu-id="6695f-103">Hálózati kapcsolat IP-konfigurációjának eltávolítása hálózati kapcsolatból.</span><span class="sxs-lookup"><span data-stu-id="6695f-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6695f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6695f-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6695f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6695f-105">DESCRIPTION</span></span>
<span data-ttu-id="6695f-106">A **Remove-AzureRmNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati felületről távolítja el.</span><span class="sxs-lookup"><span data-stu-id="6695f-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="6695f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6695f-107">EXAMPLES</span></span>

### <span data-ttu-id="6695f-108">1: IP-konfiguráció törlése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="6695f-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="6695f-109">Az első parancs a mynic nevű hálózati felületet kapja, és a változó $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="6695f-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="6695f-110">A második parancs eltávolítja az e hálózati csatolóval társított IPConfig-1 nevű IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="6695f-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="6695f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6695f-111">PARAMETERS</span></span>

### <span data-ttu-id="6695f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6695f-112">-DefaultProfile</span></span>
<span data-ttu-id="6695f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6695f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6695f-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6695f-114">-Name</span></span>
<span data-ttu-id="6695f-115">Annak a hálózati kapcsolatnak az IP-konfigurációjának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="6695f-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="6695f-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6695f-116">-NetworkInterface</span></span>
<span data-ttu-id="6695f-117">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6695f-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="6695f-118">Ez az objektum az eltávolítandó hálózati kapcsolat IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6695f-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="6695f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6695f-119">CommonParameters</span></span>
<span data-ttu-id="6695f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6695f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6695f-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6695f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6695f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6695f-122">INPUTS</span></span>

### <span data-ttu-id="6695f-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6695f-123">PSNetworkInterface</span></span>
<span data-ttu-id="6695f-124">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6695f-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="6695f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6695f-125">OUTPUTS</span></span>

### <span data-ttu-id="6695f-126">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6695f-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6695f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6695f-127">NOTES</span></span>
* <span data-ttu-id="6695f-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="6695f-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6695f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6695f-129">RELATED LINKS</span></span>

[<span data-ttu-id="6695f-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6695f-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6695f-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6695f-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6695f-132">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6695f-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6695f-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6695f-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


