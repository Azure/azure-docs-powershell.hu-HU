---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480328"
---
# <span data-ttu-id="c1218-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1218-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c1218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1218-102">SYNOPSIS</span></span>
<span data-ttu-id="c1218-103">Virtuális hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="c1218-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="c1218-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1218-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1218-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1218-105">DESCRIPTION</span></span>
<span data-ttu-id="c1218-106">A virtuális hálózati átjáró az azure-beli átjárót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="c1218-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c1218-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-ban található átjáró objektumát adja vissza a Név és az Erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="c1218-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c1218-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1218-108">EXAMPLES</span></span>

### <span data-ttu-id="c1218-109">1. példa: Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="c1218-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="c1218-110">A virtuális hálózati átjáró "myGateway1" nevű objektumát adja eredményül a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="c1218-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="c1218-111">2. példa: Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="c1218-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="c1218-112">Visszaadja az összes virtuális hálózati átjárót, amely a "myGateway" kezdetével kezdődik a "myRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c1218-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="c1218-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1218-113">PARAMETERS</span></span>

### <span data-ttu-id="c1218-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1218-114">-DefaultProfile</span></span>
<span data-ttu-id="c1218-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1218-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1218-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c1218-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c1218-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1218-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c1218-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1218-118">CommonParameters</span></span>
<span data-ttu-id="c1218-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1218-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1218-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1218-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1218-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1218-121">INPUTS</span></span>

### <span data-ttu-id="c1218-122">System.String</span><span class="sxs-lookup"><span data-stu-id="c1218-122">System.String</span></span>

## <span data-ttu-id="c1218-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1218-123">OUTPUTS</span></span>

### <span data-ttu-id="c1218-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1218-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c1218-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1218-125">NOTES</span></span>

## <span data-ttu-id="c1218-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1218-126">RELATED LINKS</span></span>

[<span data-ttu-id="c1218-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1218-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1218-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1218-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1218-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1218-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1218-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1218-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c1218-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1218-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
