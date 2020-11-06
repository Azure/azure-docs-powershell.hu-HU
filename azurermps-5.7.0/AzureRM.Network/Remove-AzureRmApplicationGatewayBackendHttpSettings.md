---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 5070d455402548888e08e85ee3e8c5629e0282a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500491"
---
# <span data-ttu-id="90682-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="90682-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="90682-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90682-102">SYNOPSIS</span></span>
<span data-ttu-id="90682-103">Eltávolítja a back-end HTTP-beállításokat egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="90682-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90682-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90682-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90682-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90682-105">DESCRIPTION</span></span>
<span data-ttu-id="90682-106">Az Remove-AzureRmApplicationGatewayBackendHttpSettings parancsmag eltávolítja a HTTP-beállításokat az Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="90682-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="90682-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90682-107">EXAMPLES</span></span>

### <span data-ttu-id="90682-108">Példa 1: a back-end HTTP-beállítások eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="90682-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="90682-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="90682-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="90682-110">A második parancs eltávolítja a BackEndSetting02 nevű back-end HTTP-beállítást az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="90682-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="90682-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90682-111">PARAMETERS</span></span>

### <span data-ttu-id="90682-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90682-112">-ApplicationGateway</span></span>
<span data-ttu-id="90682-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja a back-end HTTP-beállításokat.</span><span class="sxs-lookup"><span data-stu-id="90682-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="90682-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90682-114">-DefaultProfile</span></span>
<span data-ttu-id="90682-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90682-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90682-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90682-116">-Name</span></span>
<span data-ttu-id="90682-117">A parancsmag által eltávolított back-end HTTP-beállítások nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90682-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90682-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90682-118">CommonParameters</span></span>
<span data-ttu-id="90682-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90682-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90682-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90682-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90682-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90682-121">INPUTS</span></span>

### <span data-ttu-id="90682-122">System. String</span><span class="sxs-lookup"><span data-stu-id="90682-122">System.String</span></span>

## <span data-ttu-id="90682-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90682-123">OUTPUTS</span></span>

### <span data-ttu-id="90682-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90682-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90682-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90682-125">NOTES</span></span>

## <span data-ttu-id="90682-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90682-126">RELATED LINKS</span></span>

[<span data-ttu-id="90682-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="90682-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="90682-128">Új – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="90682-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="90682-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="90682-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="90682-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="90682-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

