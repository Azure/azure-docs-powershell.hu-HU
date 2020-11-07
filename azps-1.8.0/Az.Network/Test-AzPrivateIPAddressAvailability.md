---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 3130aec4a5032fd62423aa35dec73d7acd6e14b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669926"
---
# <span data-ttu-id="99e24-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="99e24-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="99e24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99e24-102">SYNOPSIS</span></span>
<span data-ttu-id="99e24-103">A privát IP-címek elérhetőségét a virtuális hálózatban tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="99e24-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="99e24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99e24-104">SYNTAX</span></span>

### <span data-ttu-id="99e24-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="99e24-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99e24-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="99e24-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99e24-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="99e24-107">DESCRIPTION</span></span>
<span data-ttu-id="99e24-108">A **AzPrivateIPAddressAvailability-** parancsmag azt vizsgálja, hogy egy megadott privát IP-cím elérhető-e virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="99e24-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="99e24-109">Ez a parancsmag az elérhető privát IP-címek listáját jeleníti meg, ha a kért privát IP-cím meg van véve.</span><span class="sxs-lookup"><span data-stu-id="99e24-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="99e24-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99e24-110">EXAMPLES</span></span>

### <span data-ttu-id="99e24-111">1. példa: annak vizsgálata, hogy az IP-cím elérhető-e a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="99e24-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="99e24-112">Ez a parancs virtuális hálózatot kap, és a pipeline operátor segítségével átadja a **teszt-AzPrivateIPAddressAvailability** , amely azt vizsgálja, hogy elérhető-e a megadott magánhálózati IP-cím.</span><span class="sxs-lookup"><span data-stu-id="99e24-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="99e24-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99e24-113">PARAMETERS</span></span>

### <span data-ttu-id="99e24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e24-114">-DefaultProfile</span></span>
<span data-ttu-id="99e24-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99e24-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99e24-116">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="99e24-116">-IPAddress</span></span>
<span data-ttu-id="99e24-117">A tesztelni kívánt IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="99e24-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="99e24-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e24-118">-ResourceGroupName</span></span>
<span data-ttu-id="99e24-119">A virtuális hálózat erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99e24-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="99e24-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99e24-120">-VirtualNetwork</span></span>
<span data-ttu-id="99e24-121">Egy **PSVirtualNetwork** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="99e24-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="99e24-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="99e24-122">-VirtualNetworkName</span></span>
<span data-ttu-id="99e24-123">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99e24-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="99e24-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e24-124">CommonParameters</span></span>
<span data-ttu-id="99e24-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99e24-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e24-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e24-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e24-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99e24-127">INPUTS</span></span>

### <span data-ttu-id="99e24-128">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99e24-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="99e24-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99e24-129">OUTPUTS</span></span>

### <span data-ttu-id="99e24-130">Microsoft. Azure. commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="99e24-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="99e24-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99e24-131">NOTES</span></span>

## <span data-ttu-id="99e24-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99e24-132">RELATED LINKS</span></span>

[<span data-ttu-id="99e24-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99e24-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


