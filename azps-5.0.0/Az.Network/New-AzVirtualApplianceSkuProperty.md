---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301433"
---
# <span data-ttu-id="ad9f8-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="ad9f8-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="ad9f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9f8-103">Adja meg az erőforráshoz tartozó hálózati virtuális készülék SKU-t.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="ad9f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad9f8-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad9f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ad9f8-106">A New-AzVirtualApplianceSkuProperties parancs a Network Virtual Appliance Resource (SKU) t határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ad9f8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad9f8-107">EXAMPLES</span></span>

### <span data-ttu-id="ad9f8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad9f8-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="ad9f8-109">Hozzon létre egy virtuális készülék SKU-tulajdonságú objektumát, amelyet New-AzNetworkVirtualAppliance paranccsal szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="ad9f8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad9f8-110">PARAMETERS</span></span>

### <span data-ttu-id="ad9f8-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ad9f8-111">-BundledScaleUnit</span></span>
<span data-ttu-id="ad9f8-112">A Köteges skála egysége.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="ad9f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9f8-113">-DefaultProfile</span></span>
<span data-ttu-id="ad9f8-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad9f8-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="ad9f8-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="ad9f8-116">A piaci hely verziója.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-116">The market place version.</span></span>

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

### <span data-ttu-id="ad9f8-117">-Szállítónév</span><span class="sxs-lookup"><span data-stu-id="ad9f8-117">-VendorName</span></span>
<span data-ttu-id="ad9f8-118">A szállító neve.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9f8-119">CommonParameters</span></span>
<span data-ttu-id="ad9f8-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad9f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9f8-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad9f8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9f8-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad9f8-122">INPUTS</span></span>

### <span data-ttu-id="ad9f8-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="ad9f8-123">None</span></span>

## <span data-ttu-id="ad9f8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad9f8-124">OUTPUTS</span></span>

### <span data-ttu-id="ad9f8-125">Microsoft. Azure. commands. Network. models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="ad9f8-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="ad9f8-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad9f8-126">NOTES</span></span>

## <span data-ttu-id="ad9f8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad9f8-127">RELATED LINKS</span></span>
