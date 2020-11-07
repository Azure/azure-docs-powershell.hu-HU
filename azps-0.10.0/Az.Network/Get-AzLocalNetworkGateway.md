---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841606"
---
# <span data-ttu-id="10574-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10574-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="10574-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10574-102">SYNOPSIS</span></span>
<span data-ttu-id="10574-103">Helyi hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="10574-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="10574-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10574-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10574-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10574-105">DESCRIPTION</span></span>
<span data-ttu-id="10574-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="10574-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="10574-107">A **Get-AzLocalNetworkGateway** parancsmag a helyszíni átjáró nevét és az erőforráscsoport neve alapján adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="10574-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="10574-108">Példák</span><span class="sxs-lookup"><span data-stu-id="10574-108">EXAMPLES</span></span>

### <span data-ttu-id="10574-109">1: helyi hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="10574-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="10574-110">A helyi hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myLocalGW" névvel</span><span class="sxs-lookup"><span data-stu-id="10574-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="10574-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10574-111">PARAMETERS</span></span>

### <span data-ttu-id="10574-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10574-112">-DefaultProfile</span></span>
<span data-ttu-id="10574-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10574-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10574-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10574-114">-Name</span></span>
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

### <span data-ttu-id="10574-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10574-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="10574-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10574-116">CommonParameters</span></span>
<span data-ttu-id="10574-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10574-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10574-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10574-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10574-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10574-119">INPUTS</span></span>

## <span data-ttu-id="10574-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10574-120">OUTPUTS</span></span>

### <span data-ttu-id="10574-121">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10574-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="10574-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10574-122">NOTES</span></span>

## <span data-ttu-id="10574-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10574-123">RELATED LINKS</span></span>

