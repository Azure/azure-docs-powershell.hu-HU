---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841517"
---
# <span data-ttu-id="f055c-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f055c-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f055c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f055c-102">SYNOPSIS</span></span>
<span data-ttu-id="f055c-103">Virtuális hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="f055c-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="f055c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f055c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f055c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f055c-105">DESCRIPTION</span></span>
<span data-ttu-id="f055c-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f055c-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="f055c-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="f055c-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f055c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f055c-108">EXAMPLES</span></span>

### <span data-ttu-id="f055c-109">1: virtuális hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="f055c-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="f055c-110">A virtuális hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myGateway" néven.</span><span class="sxs-lookup"><span data-stu-id="f055c-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="f055c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f055c-111">PARAMETERS</span></span>

### <span data-ttu-id="f055c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f055c-112">-DefaultProfile</span></span>
<span data-ttu-id="f055c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f055c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f055c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f055c-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f055c-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f055c-116">CommonParameters</span></span>
<span data-ttu-id="f055c-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f055c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f055c-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f055c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f055c-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f055c-119">INPUTS</span></span>

## <span data-ttu-id="f055c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f055c-120">OUTPUTS</span></span>

### <span data-ttu-id="f055c-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f055c-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f055c-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f055c-122">NOTES</span></span>

## <span data-ttu-id="f055c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f055c-123">RELATED LINKS</span></span>

