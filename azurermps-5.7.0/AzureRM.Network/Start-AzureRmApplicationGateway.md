---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 2faa1b245a38a5ef66bb5131f79000218c39d55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501463"
---
# <span data-ttu-id="51ce4-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51ce4-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="51ce4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="51ce4-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="51ce4-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51ce4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51ce4-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ce4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="51ce4-106">A **Start-AzureRmApplicationGateway** parancsmag az Azure Application Gatewayt indítja el.</span><span class="sxs-lookup"><span data-stu-id="51ce4-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="51ce4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51ce4-107">EXAMPLES</span></span>

### <span data-ttu-id="51ce4-108">Example1: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="51ce4-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="51ce4-109">Ez a parancs elindítja az $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="51ce4-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="51ce4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51ce4-110">PARAMETERS</span></span>

### <span data-ttu-id="51ce4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51ce4-111">-ApplicationGateway</span></span>
<span data-ttu-id="51ce4-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="51ce4-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51ce4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ce4-113">-DefaultProfile</span></span>
<span data-ttu-id="51ce4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51ce4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51ce4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ce4-115">CommonParameters</span></span>
<span data-ttu-id="51ce4-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51ce4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ce4-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51ce4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ce4-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51ce4-118">INPUTS</span></span>

### <span data-ttu-id="51ce4-119">System. String</span><span class="sxs-lookup"><span data-stu-id="51ce4-119">System.String</span></span>

## <span data-ttu-id="51ce4-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51ce4-120">OUTPUTS</span></span>

### <span data-ttu-id="51ce4-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51ce4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="51ce4-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51ce4-122">NOTES</span></span>

## <span data-ttu-id="51ce4-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51ce4-123">RELATED LINKS</span></span>

[<span data-ttu-id="51ce4-124">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51ce4-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


