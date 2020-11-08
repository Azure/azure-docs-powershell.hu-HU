---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194050"
---
# <span data-ttu-id="82415-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82415-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="82415-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82415-102">SYNOPSIS</span></span>
<span data-ttu-id="82415-103">Virtuális hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="82415-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="82415-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82415-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82415-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82415-105">DESCRIPTION</span></span>
<span data-ttu-id="82415-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="82415-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="82415-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="82415-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="82415-108">Példák</span><span class="sxs-lookup"><span data-stu-id="82415-108">EXAMPLES</span></span>

### <span data-ttu-id="82415-109">Példa 1: virtuális hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="82415-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="82415-110">A virtuális hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myGateway1" néven.</span><span class="sxs-lookup"><span data-stu-id="82415-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="82415-111">2. példa: virtuális hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="82415-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="82415-112">Azokat a virtuális hálózati átjárókat számítja ki, amelyek az "myRG" erőforráscsoporthoz tartozó "myGateway" csoporttal kezdődnek</span><span class="sxs-lookup"><span data-stu-id="82415-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="82415-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82415-113">PARAMETERS</span></span>

### <span data-ttu-id="82415-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82415-114">-DefaultProfile</span></span>
<span data-ttu-id="82415-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82415-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82415-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82415-116">-Name</span></span>
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

### <span data-ttu-id="82415-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82415-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="82415-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82415-118">CommonParameters</span></span>
<span data-ttu-id="82415-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82415-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82415-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="82415-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82415-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82415-121">INPUTS</span></span>

### <span data-ttu-id="82415-122">System. String</span><span class="sxs-lookup"><span data-stu-id="82415-122">System.String</span></span>

## <span data-ttu-id="82415-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82415-123">OUTPUTS</span></span>

### <span data-ttu-id="82415-124">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82415-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="82415-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82415-125">NOTES</span></span>

## <span data-ttu-id="82415-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82415-126">RELATED LINKS</span></span>

[<span data-ttu-id="82415-127">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82415-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="82415-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82415-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="82415-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82415-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="82415-130">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82415-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="82415-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82415-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
