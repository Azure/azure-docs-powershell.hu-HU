---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 6a5ee3b03a4242c3c11d5c34da4a333ee7c82843
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843505"
---
# <span data-ttu-id="16981-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="16981-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="16981-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16981-102">SYNOPSIS</span></span>
<span data-ttu-id="16981-103">A privát IP-címek elérhetőségét a virtuális hálózatban tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="16981-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="16981-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16981-104">SYNTAX</span></span>

### <span data-ttu-id="16981-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="16981-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16981-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="16981-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16981-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="16981-107">DESCRIPTION</span></span>
<span data-ttu-id="16981-108">A **AzPrivateIPAddressAvailability-** parancsmag azt vizsgálja, hogy egy megadott privát IP-cím elérhető-e virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="16981-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="16981-109">Ez a parancsmag az elérhető privát IP-címek listáját jeleníti meg, ha a kért privát IP-cím meg van véve.</span><span class="sxs-lookup"><span data-stu-id="16981-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="16981-110">Példák</span><span class="sxs-lookup"><span data-stu-id="16981-110">EXAMPLES</span></span>

### <span data-ttu-id="16981-111">1. példa: annak vizsgálata, hogy az IP-cím elérhető-e a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="16981-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="16981-112">Ez a parancs virtuális hálózatot kap, és a pipeline operátor segítségével átadja a **teszt-AzPrivateIPAddressAvailability** , amely azt vizsgálja, hogy elérhető-e a megadott magánhálózati IP-cím.</span><span class="sxs-lookup"><span data-stu-id="16981-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="16981-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16981-113">PARAMETERS</span></span>

### <span data-ttu-id="16981-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16981-114">-DefaultProfile</span></span>
<span data-ttu-id="16981-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16981-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16981-116">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="16981-116">-IPAddress</span></span>
<span data-ttu-id="16981-117">A tesztelni kívánt IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="16981-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="16981-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16981-118">-ResourceGroupName</span></span>
<span data-ttu-id="16981-119">A virtuális hálózat erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16981-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="16981-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="16981-120">-VirtualNetwork</span></span>
<span data-ttu-id="16981-121">Egy **PSVirtualNetwork** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="16981-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="16981-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="16981-122">-VirtualNetworkName</span></span>
<span data-ttu-id="16981-123">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16981-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="16981-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16981-124">CommonParameters</span></span>
<span data-ttu-id="16981-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16981-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16981-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16981-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16981-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16981-127">INPUTS</span></span>

### <span data-ttu-id="16981-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="16981-128">PSVirtualNetwork</span></span>
<span data-ttu-id="16981-129">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="16981-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="16981-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16981-130">OUTPUTS</span></span>

### <span data-ttu-id="16981-131">Microsoft. Azure. commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="16981-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="16981-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16981-132">NOTES</span></span>

## <span data-ttu-id="16981-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16981-133">RELATED LINKS</span></span>

[<span data-ttu-id="16981-134">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="16981-134">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


