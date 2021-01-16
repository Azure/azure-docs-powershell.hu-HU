---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326210"
---
# <span data-ttu-id="ec417-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ec417-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="ec417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec417-102">SYNOPSIS</span></span>
<span data-ttu-id="ec417-103">Eltávolítja a háttér-HTTP-beállításokat egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="ec417-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="ec417-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec417-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec417-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec417-105">DESCRIPTION</span></span>
<span data-ttu-id="ec417-106">A Remove-AzApplicationGatewayBackendHttpSetting parancsmag eltávolítja a háttér-hypertext Transfer Protocol (HTTP) beállításait egy Azure-alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="ec417-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="ec417-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec417-107">EXAMPLES</span></span>

### <span data-ttu-id="ec417-108">1. példa: Háttér-HTTP-beállítások eltávolítása alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="ec417-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="ec417-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="ec417-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec417-110">A második parancs eltávolítja a BackEndSetting02 nevű háttér-HTTP-beállítást a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ec417-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ec417-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec417-111">PARAMETERS</span></span>

### <span data-ttu-id="ec417-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec417-112">-ApplicationGateway</span></span>
<span data-ttu-id="ec417-113">Azt az alkalmazás-átjárót adja meg, amelyből a parancsmag eltávolítja a háttér HTTP-beállításait.</span><span class="sxs-lookup"><span data-stu-id="ec417-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec417-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec417-114">-DefaultProfile</span></span>
<span data-ttu-id="ec417-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec417-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec417-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ec417-116">-Name</span></span>
<span data-ttu-id="ec417-117">A parancsmag által eltávolított háttér-HTTP-beállítások nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec417-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec417-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec417-118">CommonParameters</span></span>
<span data-ttu-id="ec417-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec417-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec417-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec417-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec417-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec417-121">INPUTS</span></span>

### <span data-ttu-id="ec417-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec417-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec417-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec417-123">OUTPUTS</span></span>

### <span data-ttu-id="ec417-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec417-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec417-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec417-125">NOTES</span></span>

## <span data-ttu-id="ec417-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec417-126">RELATED LINKS</span></span>

[<span data-ttu-id="ec417-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ec417-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ec417-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ec417-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ec417-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ec417-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ec417-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ec417-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

