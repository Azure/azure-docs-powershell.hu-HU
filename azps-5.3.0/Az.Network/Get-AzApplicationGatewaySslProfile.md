---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468169"
---
# <span data-ttu-id="12229-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="12229-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="12229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12229-102">SYNOPSIS</span></span>
<span data-ttu-id="12229-103">Egy alkalmazás-átjáró SSL-profilját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12229-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="12229-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12229-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12229-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12229-105">DESCRIPTION</span></span>
<span data-ttu-id="12229-106">A **Get-AzApplicationGatewaySslProfile** parancsmag egy alkalmazás-átjáró SSL-profilját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12229-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="12229-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12229-107">EXAMPLES</span></span>

### <span data-ttu-id="12229-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="12229-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="12229-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs az SSL-profil SslProfile01-et kap a $AppGw és tárolja a $profile változóban.</span><span class="sxs-lookup"><span data-stu-id="12229-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="12229-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12229-110">PARAMETERS</span></span>

### <span data-ttu-id="12229-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12229-111">-ApplicationGateway</span></span>
<span data-ttu-id="12229-112">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="12229-112">The applicationGateway</span></span>

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

### <span data-ttu-id="12229-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12229-113">-DefaultProfile</span></span>
<span data-ttu-id="12229-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12229-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12229-115">-Name</span><span class="sxs-lookup"><span data-stu-id="12229-115">-Name</span></span>
<span data-ttu-id="12229-116">Az ssl-profil neve</span><span class="sxs-lookup"><span data-stu-id="12229-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="12229-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12229-117">CommonParameters</span></span>
<span data-ttu-id="12229-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12229-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12229-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12229-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12229-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12229-120">INPUTS</span></span>

### <span data-ttu-id="12229-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12229-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12229-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12229-122">OUTPUTS</span></span>

### <span data-ttu-id="12229-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="12229-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="12229-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12229-124">NOTES</span></span>

## <span data-ttu-id="12229-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12229-125">RELATED LINKS</span></span>

[<span data-ttu-id="12229-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="12229-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="12229-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="12229-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="12229-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="12229-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="12229-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="12229-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)