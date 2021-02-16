---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160795"
---
# <span data-ttu-id="6e0fa-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="6e0fa-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="6e0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0fa-103">Definiáljon egy hálózati virtuális eszköz termékváltozatot az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="6e0fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e0fa-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e0fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e0fa-105">DESCRIPTION</span></span>
<span data-ttu-id="6e0fa-106">A New-AzVirtualApplianceSkuProperties parancs meghatároz egy termékváltozatot a hálózati virtuális eszköz erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6e0fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e0fa-107">EXAMPLES</span></span>

### <span data-ttu-id="6e0fa-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6e0fa-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="6e0fa-109">Hozzon létre egy virtuális berendezés-termékváltozat tulajdonságai objektumot, amely a New-AzNetworkVirtualAppliance használható.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="6e0fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e0fa-110">PARAMETERS</span></span>

### <span data-ttu-id="6e0fa-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6e0fa-111">-BundledScaleUnit</span></span>
<span data-ttu-id="6e0fa-112">A kötegelt méretarány.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="6e0fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0fa-113">-DefaultProfile</span></span>
<span data-ttu-id="6e0fa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e0fa-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="6e0fa-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="6e0fa-116">A piachely verziója.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-116">The market place version.</span></span>

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

### <span data-ttu-id="6e0fa-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="6e0fa-117">-VendorName</span></span>
<span data-ttu-id="6e0fa-118">A szállító neve.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="6e0fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0fa-119">CommonParameters</span></span>
<span data-ttu-id="6e0fa-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0fa-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e0fa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0fa-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e0fa-122">INPUTS</span></span>

### <span data-ttu-id="6e0fa-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="6e0fa-123">None</span></span>

## <span data-ttu-id="6e0fa-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e0fa-124">OUTPUTS</span></span>

### <span data-ttu-id="6e0fa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="6e0fa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="6e0fa-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e0fa-126">NOTES</span></span>

## <span data-ttu-id="6e0fa-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e0fa-127">RELATED LINKS</span></span>
