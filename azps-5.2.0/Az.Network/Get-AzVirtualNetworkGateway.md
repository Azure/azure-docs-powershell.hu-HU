---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356082"
---
# <span data-ttu-id="29a3e-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29a3e-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="29a3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="29a3e-103">Virtuális hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="29a3e-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="29a3e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29a3e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29a3e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="29a3e-106">A virtuális hálózati átjáró az azure-beli átjárót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="29a3e-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="29a3e-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-ban található átjáró objektumát adja vissza a Név és az Erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="29a3e-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="29a3e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29a3e-108">EXAMPLES</span></span>

### <span data-ttu-id="29a3e-109">1. példa: Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="29a3e-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="29a3e-110">A virtuális hálózati átjáró "myGateway1" nevű objektumát adja eredményül a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="29a3e-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="29a3e-111">2. példa: Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="29a3e-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="29a3e-112">Visszaadja az összes virtuális hálózati átjárót, amely a "myGateway" kezdetével kezdődik a "myRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="29a3e-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="29a3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29a3e-113">PARAMETERS</span></span>

### <span data-ttu-id="29a3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a3e-114">-DefaultProfile</span></span>
<span data-ttu-id="29a3e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29a3e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29a3e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="29a3e-116">-Name</span></span>
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

### <span data-ttu-id="29a3e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a3e-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="29a3e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a3e-118">CommonParameters</span></span>
<span data-ttu-id="29a3e-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a3e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a3e-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29a3e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a3e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29a3e-121">INPUTS</span></span>

### <span data-ttu-id="29a3e-122">System.String</span><span class="sxs-lookup"><span data-stu-id="29a3e-122">System.String</span></span>

## <span data-ttu-id="29a3e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29a3e-123">OUTPUTS</span></span>

### <span data-ttu-id="29a3e-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29a3e-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="29a3e-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29a3e-125">NOTES</span></span>

## <span data-ttu-id="29a3e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29a3e-126">RELATED LINKS</span></span>

[<span data-ttu-id="29a3e-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29a3e-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="29a3e-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29a3e-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="29a3e-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29a3e-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="29a3e-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29a3e-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="29a3e-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="29a3e-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
