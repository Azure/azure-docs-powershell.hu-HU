---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: c9443c93745c1f6db9372b8f845f3ac399e51398
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841714"
---
# <span data-ttu-id="26be1-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26be1-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="26be1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26be1-102">SYNOPSIS</span></span>
<span data-ttu-id="26be1-103">Meglévő átirányítási konfigurációt kap egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="26be1-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="26be1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26be1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26be1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26be1-105">DESCRIPTION</span></span>
<span data-ttu-id="26be1-106">A **Get-AzApplicationGatewayRedirectConfiguration** parancsmag egy meglévő átirányítási konfigurációt kap egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="26be1-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="26be1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26be1-107">EXAMPLES</span></span>

### <span data-ttu-id="26be1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26be1-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="26be1-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="26be1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="26be1-110">A második parancs a Redirect01 nevű átirányítási konfigurációt a $AppGW nevű változóban tárolt alkalmazás-átjáróról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26be1-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="26be1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26be1-111">PARAMETERS</span></span>

### <span data-ttu-id="26be1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26be1-112">-ApplicationGateway</span></span>
<span data-ttu-id="26be1-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="26be1-113">The applicationGateway</span></span>

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

### <span data-ttu-id="26be1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26be1-114">-DefaultProfile</span></span>
<span data-ttu-id="26be1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26be1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26be1-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26be1-116">-Name</span></span>
<span data-ttu-id="26be1-117">A kérés útválasztási szabályának neve</span><span class="sxs-lookup"><span data-stu-id="26be1-117">The name of the request routing rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26be1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26be1-118">CommonParameters</span></span>
<span data-ttu-id="26be1-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26be1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26be1-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26be1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26be1-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26be1-121">INPUTS</span></span>

### <span data-ttu-id="26be1-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26be1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26be1-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26be1-123">OUTPUTS</span></span>

### <span data-ttu-id="26be1-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26be1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="26be1-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. commands. Network, Version = 4.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="26be1-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="26be1-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26be1-126">NOTES</span></span>

## <span data-ttu-id="26be1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26be1-127">RELATED LINKS</span></span>

