---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845906"
---
# <span data-ttu-id="64d0f-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="64d0f-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="64d0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="64d0f-103">A privát IP-címek elérhetőségét a virtuális hálózatban tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="64d0f-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="64d0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64d0f-104">SYNTAX</span></span>

### <span data-ttu-id="64d0f-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="64d0f-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64d0f-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="64d0f-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64d0f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="64d0f-107">DESCRIPTION</span></span>
<span data-ttu-id="64d0f-108">A **AzPrivateIPAddressAvailability-** parancsmag azt vizsgálja, hogy egy megadott privát IP-cím elérhető-e virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="64d0f-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="64d0f-109">Ez a parancsmag az elérhető privát IP-címek listáját jeleníti meg, ha a kért privát IP-cím meg van véve.</span><span class="sxs-lookup"><span data-stu-id="64d0f-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="64d0f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64d0f-110">EXAMPLES</span></span>

### <span data-ttu-id="64d0f-111">1. példa: annak vizsgálata, hogy az IP-cím elérhető-e a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="64d0f-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="64d0f-112">Ez a parancs virtuális hálózatot kap, és a pipeline operátor segítségével átadja a **teszt-AzPrivateIPAddressAvailability** , amely azt vizsgálja, hogy elérhető-e a megadott magánhálózati IP-cím.</span><span class="sxs-lookup"><span data-stu-id="64d0f-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="64d0f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64d0f-113">PARAMETERS</span></span>

### <span data-ttu-id="64d0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d0f-114">-DefaultProfile</span></span>
<span data-ttu-id="64d0f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64d0f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d0f-116">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="64d0f-116">-IPAddress</span></span>
<span data-ttu-id="64d0f-117">A tesztelni kívánt IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="64d0f-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="64d0f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d0f-118">-ResourceGroupName</span></span>
<span data-ttu-id="64d0f-119">A virtuális hálózat erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64d0f-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d0f-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64d0f-120">-VirtualNetwork</span></span>
<span data-ttu-id="64d0f-121">Egy **PSVirtualNetwork** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="64d0f-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64d0f-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="64d0f-122">-VirtualNetworkName</span></span>
<span data-ttu-id="64d0f-123">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64d0f-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d0f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d0f-124">CommonParameters</span></span>
<span data-ttu-id="64d0f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64d0f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d0f-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d0f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d0f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64d0f-127">INPUTS</span></span>

### <span data-ttu-id="64d0f-128">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64d0f-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="64d0f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64d0f-129">OUTPUTS</span></span>

### <span data-ttu-id="64d0f-130">Microsoft. Azure. commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="64d0f-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="64d0f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64d0f-131">NOTES</span></span>

## <span data-ttu-id="64d0f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64d0f-132">RELATED LINKS</span></span>

[<span data-ttu-id="64d0f-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64d0f-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


