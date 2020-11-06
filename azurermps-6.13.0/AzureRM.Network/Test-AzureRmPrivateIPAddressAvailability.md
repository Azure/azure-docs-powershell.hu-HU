---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 2367f57db4e028710dce18acacd5b644b41f335b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498267"
---
# <span data-ttu-id="3f904-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="3f904-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="3f904-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f904-102">SYNOPSIS</span></span>
<span data-ttu-id="3f904-103">A privát IP-címek elérhetőségét a virtuális hálózatban tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="3f904-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f904-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f904-104">SYNTAX</span></span>

### <span data-ttu-id="3f904-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="3f904-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f904-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f904-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f904-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f904-107">DESCRIPTION</span></span>
<span data-ttu-id="3f904-108">A **AzureRmPrivateIPAddressAvailability-** parancsmag azt vizsgálja, hogy egy megadott privát IP-cím elérhető-e virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="3f904-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="3f904-109">Ez a parancsmag az elérhető privát IP-címek listáját jeleníti meg, ha a kért privát IP-cím meg van véve.</span><span class="sxs-lookup"><span data-stu-id="3f904-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="3f904-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3f904-110">EXAMPLES</span></span>

### <span data-ttu-id="3f904-111">1. példa: annak vizsgálata, hogy az IP-cím elérhető-e a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="3f904-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="3f904-112">Ez a parancs virtuális hálózatot kap, és a pipeline operátor segítségével átadja a **teszt-AzureRmPrivateIPAddressAvailability** , amely azt vizsgálja, hogy elérhető-e a megadott magánhálózati IP-cím.</span><span class="sxs-lookup"><span data-stu-id="3f904-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="3f904-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f904-113">PARAMETERS</span></span>

### <span data-ttu-id="3f904-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f904-114">-DefaultProfile</span></span>
<span data-ttu-id="3f904-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f904-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f904-116">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="3f904-116">-IPAddress</span></span>
<span data-ttu-id="3f904-117">A tesztelni kívánt IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f904-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="3f904-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f904-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f904-119">A virtuális hálózat erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f904-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="3f904-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f904-120">-VirtualNetwork</span></span>
<span data-ttu-id="3f904-121">Egy **PSVirtualNetwork** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3f904-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="3f904-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3f904-122">-VirtualNetworkName</span></span>
<span data-ttu-id="3f904-123">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f904-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="3f904-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f904-124">CommonParameters</span></span>
<span data-ttu-id="3f904-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f904-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f904-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f904-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f904-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f904-127">INPUTS</span></span>

### <span data-ttu-id="3f904-128">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f904-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="3f904-129">Paraméterek: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3f904-129">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="3f904-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f904-130">OUTPUTS</span></span>

### <span data-ttu-id="3f904-131">Microsoft. Azure. commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="3f904-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="3f904-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f904-132">NOTES</span></span>

## <span data-ttu-id="3f904-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f904-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f904-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f904-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


