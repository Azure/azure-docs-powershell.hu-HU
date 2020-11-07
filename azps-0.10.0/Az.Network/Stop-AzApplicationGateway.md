---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 97dc4b46f4a9156bc43e7902d50414a586d0f337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843530"
---
# <span data-ttu-id="ccaa1-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="ccaa1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="ccaa1-103">Az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="ccaa1-103">Stops an application gateway</span></span>

## <span data-ttu-id="ccaa1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccaa1-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccaa1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccaa1-105">DESCRIPTION</span></span>
<span data-ttu-id="ccaa1-106">A **stop-AzApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="ccaa1-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="ccaa1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccaa1-107">EXAMPLES</span></span>

### <span data-ttu-id="ccaa1-108">1. példa: az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="ccaa1-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="ccaa1-109">Ez a parancs leállítja a $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="ccaa1-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="ccaa1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccaa1-110">PARAMETERS</span></span>

### <span data-ttu-id="ccaa1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-111">-ApplicationGateway</span></span>
<span data-ttu-id="ccaa1-112">Annak az alkalmazásnak az átjáróját adja meg, amely a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="ccaa1-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ccaa1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccaa1-113">-AsJob</span></span>
<span data-ttu-id="ccaa1-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ccaa1-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaa1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccaa1-115">-DefaultProfile</span></span>
<span data-ttu-id="ccaa1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccaa1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccaa1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccaa1-117">CommonParameters</span></span>
<span data-ttu-id="ccaa1-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccaa1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccaa1-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccaa1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccaa1-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccaa1-120">INPUTS</span></span>

### <span data-ttu-id="ccaa1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ccaa1-121">System.String</span></span>

## <span data-ttu-id="ccaa1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccaa1-122">OUTPUTS</span></span>

### <span data-ttu-id="ccaa1-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ccaa1-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccaa1-124">NOTES</span></span>

## <span data-ttu-id="ccaa1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccaa1-125">RELATED LINKS</span></span>

[<span data-ttu-id="ccaa1-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ccaa1-127">Új – AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="ccaa1-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="ccaa1-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="ccaa1-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccaa1-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


