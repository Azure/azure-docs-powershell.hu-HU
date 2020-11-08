---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181575"
---
# <span data-ttu-id="50893-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="50893-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="50893-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50893-102">SYNOPSIS</span></span>
<span data-ttu-id="50893-103">új IpconfigurationBgpPeeringAddressObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="50893-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="50893-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50893-104">SYNTAX</span></span>

### <span data-ttu-id="50893-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50893-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="50893-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="50893-106">DESCRIPTION</span></span>
<span data-ttu-id="50893-107">A **New-AzIpConfigurationBgpPeeringAddressObject** létrehoz egy IpConfigurationBgpPeeringAddressObject objektumot, amely a virtuális hálózati átjáró bgpsettings BgpPeeringAddresses tulajdonságát képviseli.</span><span class="sxs-lookup"><span data-stu-id="50893-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="50893-108">Példák</span><span class="sxs-lookup"><span data-stu-id="50893-108">EXAMPLES</span></span>

### <span data-ttu-id="50893-109">1: AzIpConfigurationBgpPeeringAddressObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="50893-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="50893-110">A fenti IpConfigurationBgpPeeringAddressObject létre fog hozni. Ez az új objektum a gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="50893-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="50893-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50893-111">PARAMETERS</span></span>

### <span data-ttu-id="50893-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50893-112">-Confirm</span></span>
<span data-ttu-id="50893-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50893-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50893-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="50893-114">-CustomAddress</span></span>
<span data-ttu-id="50893-115">A BgpPeeringAddresses virtuális hálózati átjáró CustomAddress listája.</span><span class="sxs-lookup"><span data-stu-id="50893-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50893-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50893-116">-DefaultProfile</span></span>
<span data-ttu-id="50893-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50893-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50893-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="50893-118">-IpConfigurationId</span></span>
<span data-ttu-id="50893-119">A virtuális hálózati átjáró IpConfigurationId a BgpPeeringAddresses-hoz.</span><span class="sxs-lookup"><span data-stu-id="50893-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="50893-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50893-120">-WhatIf</span></span>
<span data-ttu-id="50893-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50893-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50893-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50893-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50893-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50893-123">CommonParameters</span></span>
<span data-ttu-id="50893-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50893-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50893-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="50893-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50893-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50893-126">INPUTS</span></span>

### <span data-ttu-id="50893-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="50893-127">None</span></span>

## <span data-ttu-id="50893-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50893-128">OUTPUTS</span></span>

### <span data-ttu-id="50893-129">Microsoft. Azure. commands. Network. models. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="50893-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="50893-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50893-130">NOTES</span></span>

## <span data-ttu-id="50893-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50893-131">RELATED LINKS</span></span>
