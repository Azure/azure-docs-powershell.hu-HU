---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 5936a7e3f15919e00fa052a2950fd31e69ca32fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841602"
---
# <span data-ttu-id="d0464-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0464-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d0464-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0464-102">SYNOPSIS</span></span>
<span data-ttu-id="d0464-103">Hálózati kapcsolat IP-konfigurációjának lekérdezése hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="d0464-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="d0464-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0464-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0464-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0464-105">DESCRIPTION</span></span>
<span data-ttu-id="d0464-106">A **Get-AzNetworkInterfaceIPConfig** parancsmag az Azure hálózati interfészből származó hálózati kapcsolat IP-konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="d0464-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="d0464-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d0464-107">EXAMPLES</span></span>

### <span data-ttu-id="d0464-108">1: hálózati felület IP-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d0464-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="d0464-109">Az első parancs beolvassa a mynic nevű meglévő hálózati felületet, és a $nic 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0464-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="d0464-110">A második parancs a hálózati kapcsolat ipconfig1 nevű IP-konfigurációt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d0464-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="d0464-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0464-111">PARAMETERS</span></span>

### <span data-ttu-id="d0464-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0464-112">-DefaultProfile</span></span>
<span data-ttu-id="d0464-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0464-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0464-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0464-114">-Name</span></span>
<span data-ttu-id="d0464-115">Annak a hálózati IP-konfigurációnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="d0464-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0464-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d0464-116">-NetworkInterface</span></span>
<span data-ttu-id="d0464-117">Itt adhatja meg azt a **NetworkInterface** -objektumot, amely a parancsmag által beolvasott hálózati IP-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d0464-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0464-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0464-118">CommonParameters</span></span>
<span data-ttu-id="d0464-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0464-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0464-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0464-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0464-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0464-121">INPUTS</span></span>

### <span data-ttu-id="d0464-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d0464-122">PSNetworkInterface</span></span>
<span data-ttu-id="d0464-123">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d0464-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="d0464-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0464-124">OUTPUTS</span></span>

### <span data-ttu-id="d0464-125">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0464-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="d0464-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0464-126">NOTES</span></span>
* <span data-ttu-id="d0464-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="d0464-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d0464-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0464-128">RELATED LINKS</span></span>

[<span data-ttu-id="d0464-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0464-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d0464-130">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0464-130">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d0464-131">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0464-131">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d0464-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0464-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


