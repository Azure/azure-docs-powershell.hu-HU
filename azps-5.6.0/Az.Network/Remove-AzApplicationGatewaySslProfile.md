---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ab8afdb01a2993330c75b23b02392ee583cad297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941713"
---
# <span data-ttu-id="0129c-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0129c-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0129c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0129c-102">SYNOPSIS</span></span>
<span data-ttu-id="0129c-103">Eltávolítja az ssl-profilt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="0129c-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="0129c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0129c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0129c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0129c-105">DESCRIPTION</span></span>
<span data-ttu-id="0129c-106">A **Remove-AzApplicationGatewaySslProfile** parancsmag eltávolítja az ssl-profilt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="0129c-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="0129c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0129c-107">EXAMPLES</span></span>

### <span data-ttu-id="0129c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0129c-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="0129c-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="0129c-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="0129c-110">A második parancs eltávolítja az SslProfile01 nevű ssl-profilt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0129c-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0129c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0129c-111">PARAMETERS</span></span>

### <span data-ttu-id="0129c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0129c-112">-ApplicationGateway</span></span>
<span data-ttu-id="0129c-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="0129c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0129c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0129c-114">-DefaultProfile</span></span>
<span data-ttu-id="0129c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0129c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0129c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0129c-116">-Name</span></span>
<span data-ttu-id="0129c-117">Az ssl-profil neve</span><span class="sxs-lookup"><span data-stu-id="0129c-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="0129c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0129c-118">CommonParameters</span></span>
<span data-ttu-id="0129c-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0129c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0129c-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0129c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0129c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0129c-121">INPUTS</span></span>

### <span data-ttu-id="0129c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0129c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0129c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0129c-123">OUTPUTS</span></span>

### <span data-ttu-id="0129c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0129c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0129c-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0129c-125">NOTES</span></span>

## <span data-ttu-id="0129c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0129c-126">RELATED LINKS</span></span>

[<span data-ttu-id="0129c-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0129c-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0129c-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0129c-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0129c-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0129c-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0129c-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0129c-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)