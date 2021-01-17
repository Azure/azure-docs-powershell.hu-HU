---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466726"
---
# <span data-ttu-id="510d2-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="510d2-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="510d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="510d2-102">SYNOPSIS</span></span>
<span data-ttu-id="510d2-103">Tesztelje a privát IP-címek elérhetőségét egy virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="510d2-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="510d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="510d2-104">SYNTAX</span></span>

### <span data-ttu-id="510d2-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="510d2-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="510d2-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="510d2-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="510d2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="510d2-107">DESCRIPTION</span></span>
<span data-ttu-id="510d2-108">A **Test-AzPrivateIPAddressAvailability** parancsmag teszteli, hogy egy megadott privát IP-cím elérhető-e virtuális hálózaton.</span><span class="sxs-lookup"><span data-stu-id="510d2-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="510d2-109">Ez a parancsmag az elérhető privát IP-címek listáját adja vissza, ha a kért privát IP-cím meg van véve.</span><span class="sxs-lookup"><span data-stu-id="510d2-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="510d2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="510d2-110">EXAMPLES</span></span>

### <span data-ttu-id="510d2-111">1. példa: Annak vizsgálata, hogy elérhető-e IP-cím a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="510d2-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="510d2-112">Ez a parancs egy virtuális hálózatot kap, és a folyamat műveleti jelével adja át a **Test-AzPrivateIPAddressAvailability** tartománynak, amely teszteli, hogy elérhető-e a megadott privát IP-cím.</span><span class="sxs-lookup"><span data-stu-id="510d2-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability**, which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="510d2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="510d2-113">PARAMETERS</span></span>

### <span data-ttu-id="510d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510d2-114">-DefaultProfile</span></span>
<span data-ttu-id="510d2-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="510d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="510d2-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="510d2-116">-IPAddress</span></span>
<span data-ttu-id="510d2-117">A tesztelni megfelelő IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="510d2-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="510d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="510d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="510d2-119">A virtuális hálózat erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="510d2-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="510d2-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="510d2-120">-VirtualNetwork</span></span>
<span data-ttu-id="510d2-121">EGY **PSVirtualNetwork objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="510d2-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="510d2-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="510d2-122">-VirtualNetworkName</span></span>
<span data-ttu-id="510d2-123">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="510d2-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="510d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510d2-124">CommonParameters</span></span>
<span data-ttu-id="510d2-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="510d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510d2-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="510d2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510d2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="510d2-127">INPUTS</span></span>

### <span data-ttu-id="510d2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="510d2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="510d2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="510d2-129">OUTPUTS</span></span>

### <span data-ttu-id="510d2-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="510d2-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="510d2-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="510d2-131">NOTES</span></span>

## <span data-ttu-id="510d2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="510d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="510d2-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="510d2-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


