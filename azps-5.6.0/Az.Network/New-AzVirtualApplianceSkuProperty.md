---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006181"
---
# <span data-ttu-id="21651-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="21651-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="21651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21651-102">SYNOPSIS</span></span>
<span data-ttu-id="21651-103">Definiáljon egy hálózati virtuális eszköz termékváltozatot az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="21651-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="21651-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21651-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21651-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21651-105">DESCRIPTION</span></span>
<span data-ttu-id="21651-106">A New-AzVirtualApplianceSkuProperties parancs meghatároz egy termékváltozatot a hálózati virtuális eszköz erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="21651-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="21651-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21651-107">EXAMPLES</span></span>

### <span data-ttu-id="21651-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="21651-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="21651-109">Hozzon létre egy virtuális berendezés-termékváltozat tulajdonságai objektumot, amely a New-AzNetworkVirtualAppliance használható.</span><span class="sxs-lookup"><span data-stu-id="21651-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="21651-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21651-110">PARAMETERS</span></span>

### <span data-ttu-id="21651-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="21651-111">-BundledScaleUnit</span></span>
<span data-ttu-id="21651-112">A kötegelt méretarány.</span><span class="sxs-lookup"><span data-stu-id="21651-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="21651-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21651-113">-DefaultProfile</span></span>
<span data-ttu-id="21651-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21651-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21651-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="21651-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="21651-116">A piachely verziója.</span><span class="sxs-lookup"><span data-stu-id="21651-116">The market place version.</span></span>

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

### <span data-ttu-id="21651-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="21651-117">-VendorName</span></span>
<span data-ttu-id="21651-118">A szállító neve.</span><span class="sxs-lookup"><span data-stu-id="21651-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="21651-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21651-119">CommonParameters</span></span>
<span data-ttu-id="21651-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21651-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21651-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21651-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21651-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21651-122">INPUTS</span></span>

### <span data-ttu-id="21651-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="21651-123">None</span></span>

## <span data-ttu-id="21651-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21651-124">OUTPUTS</span></span>

### <span data-ttu-id="21651-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="21651-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="21651-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21651-126">NOTES</span></span>

## <span data-ttu-id="21651-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21651-127">RELATED LINKS</span></span>
