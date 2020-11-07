---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
ms.openlocfilehash: 73924c1d1308a4cf457033e27e49ad7f9e19392e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848658"
---
# <span data-ttu-id="d99ef-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="d99ef-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="d99ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d99ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d99ef-103">A privát IP-címek elérhetőségét a virtuális hálózatban tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="d99ef-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d99ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d99ef-104">SYNTAX</span></span>

### <span data-ttu-id="d99ef-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="d99ef-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d99ef-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="d99ef-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d99ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d99ef-107">DESCRIPTION</span></span>
<span data-ttu-id="d99ef-108">A **AzureRmPrivateIPAddressAvailability-** parancsmag azt vizsgálja, hogy egy megadott privát IP-cím elérhető-e virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="d99ef-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="d99ef-109">Ez a parancsmag az elérhető privát IP-címek listáját jeleníti meg, ha a kért privát IP-cím meg van véve.</span><span class="sxs-lookup"><span data-stu-id="d99ef-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="d99ef-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d99ef-110">EXAMPLES</span></span>

### <span data-ttu-id="d99ef-111">1. példa: annak vizsgálata, hogy az IP-cím elérhető-e a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="d99ef-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="d99ef-112">Ez a parancs virtuális hálózatot kap, és a pipeline operátor segítségével átadja a **teszt-AzureRmPrivateIPAddressAvailability** , amely azt vizsgálja, hogy elérhető-e a megadott magánhálózati IP-cím.</span><span class="sxs-lookup"><span data-stu-id="d99ef-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="d99ef-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d99ef-113">PARAMETERS</span></span>

### <span data-ttu-id="d99ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99ef-114">-DefaultProfile</span></span>
<span data-ttu-id="d99ef-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d99ef-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d99ef-116">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="d99ef-116">-IPAddress</span></span>
<span data-ttu-id="d99ef-117">A tesztelni kívánt IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d99ef-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="d99ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d99ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="d99ef-119">A virtuális hálózat erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d99ef-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99ef-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d99ef-120">-VirtualNetwork</span></span>
<span data-ttu-id="d99ef-121">Egy **PSVirtualNetwork** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d99ef-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d99ef-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d99ef-122">-VirtualNetworkName</span></span>
<span data-ttu-id="d99ef-123">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d99ef-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99ef-124">CommonParameters</span></span>
<span data-ttu-id="d99ef-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d99ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99ef-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d99ef-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99ef-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d99ef-127">INPUTS</span></span>

### <span data-ttu-id="d99ef-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d99ef-128">PSVirtualNetwork</span></span>
<span data-ttu-id="d99ef-129">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d99ef-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="d99ef-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d99ef-130">OUTPUTS</span></span>

### <span data-ttu-id="d99ef-131">Microsoft. Azure. commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="d99ef-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="d99ef-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d99ef-132">NOTES</span></span>

## <span data-ttu-id="d99ef-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d99ef-133">RELATED LINKS</span></span>

[<span data-ttu-id="d99ef-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d99ef-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


