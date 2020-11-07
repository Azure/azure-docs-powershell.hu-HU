---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 8c37ed72659c8b5ab00d54a7ecbe9622cb9f553b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843534"
---
# <span data-ttu-id="27512-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27512-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="27512-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27512-102">SYNOPSIS</span></span>
<span data-ttu-id="27512-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="27512-103">Starts an application gateway.</span></span>

## <span data-ttu-id="27512-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27512-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27512-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27512-105">DESCRIPTION</span></span>
<span data-ttu-id="27512-106">A **Start-AzApplicationGateway** parancsmag az Azure Application Gatewayt indítja el.</span><span class="sxs-lookup"><span data-stu-id="27512-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="27512-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27512-107">EXAMPLES</span></span>

### <span data-ttu-id="27512-108">Example1: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="27512-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="27512-109">Ez a parancs elindítja az $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="27512-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="27512-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27512-110">PARAMETERS</span></span>

### <span data-ttu-id="27512-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27512-111">-ApplicationGateway</span></span>
<span data-ttu-id="27512-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="27512-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="27512-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27512-113">-DefaultProfile</span></span>
<span data-ttu-id="27512-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27512-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27512-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27512-115">CommonParameters</span></span>
<span data-ttu-id="27512-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27512-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27512-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27512-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27512-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27512-118">INPUTS</span></span>

### <span data-ttu-id="27512-119">System. String</span><span class="sxs-lookup"><span data-stu-id="27512-119">System.String</span></span>

## <span data-ttu-id="27512-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27512-120">OUTPUTS</span></span>

### <span data-ttu-id="27512-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27512-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="27512-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27512-122">NOTES</span></span>

## <span data-ttu-id="27512-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27512-123">RELATED LINKS</span></span>

[<span data-ttu-id="27512-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27512-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


