---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: eac8a985cfcb531247fcf2617fee86da92ea0112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505760"
---
# <span data-ttu-id="bca4b-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bca4b-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="bca4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bca4b-102">SYNOPSIS</span></span>
<span data-ttu-id="bca4b-103">Hálózati kapcsolat IP-konfigurációjának lekérdezése hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="bca4b-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bca4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bca4b-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bca4b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bca4b-105">DESCRIPTION</span></span>
<span data-ttu-id="bca4b-106">A **Get-AzureRmNetworkInterfaceIPConfig** parancsmag az Azure hálózati interfészből származó hálózati kapcsolat IP-konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="bca4b-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="bca4b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bca4b-107">EXAMPLES</span></span>

### <span data-ttu-id="bca4b-108">1: hálózati felület IP-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bca4b-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="bca4b-109">Az első parancs beolvassa a mynic nevű meglévő hálózati felületet, és a $nic 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bca4b-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="bca4b-110">A második parancs a hálózati kapcsolat ipconfig1 nevű IP-konfigurációt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bca4b-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="bca4b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bca4b-111">PARAMETERS</span></span>

### <span data-ttu-id="bca4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca4b-112">-DefaultProfile</span></span>
<span data-ttu-id="bca4b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bca4b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bca4b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bca4b-114">-Name</span></span>
<span data-ttu-id="bca4b-115">Annak a hálózati IP-konfigurációnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="bca4b-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bca4b-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bca4b-116">-NetworkInterface</span></span>
<span data-ttu-id="bca4b-117">Itt adhatja meg azt a **NetworkInterface** -objektumot, amely a parancsmag által beolvasott hálózati IP-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bca4b-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bca4b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca4b-118">CommonParameters</span></span>
<span data-ttu-id="bca4b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bca4b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca4b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca4b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca4b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bca4b-121">INPUTS</span></span>

### <span data-ttu-id="bca4b-122">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bca4b-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="bca4b-123">Paraméterek: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bca4b-123">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="bca4b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bca4b-124">OUTPUTS</span></span>

### <span data-ttu-id="bca4b-125">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bca4b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="bca4b-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bca4b-126">NOTES</span></span>
* <span data-ttu-id="bca4b-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="bca4b-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bca4b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bca4b-128">RELATED LINKS</span></span>

[<span data-ttu-id="bca4b-129">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bca4b-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bca4b-130">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bca4b-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bca4b-131">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bca4b-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bca4b-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bca4b-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


