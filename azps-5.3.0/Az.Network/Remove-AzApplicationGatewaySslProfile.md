---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466732"
---
# <span data-ttu-id="4e506-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4e506-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="4e506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e506-102">SYNOPSIS</span></span>
<span data-ttu-id="4e506-103">Eltávolítja az ssl-profilt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="4e506-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="4e506-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e506-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e506-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e506-105">DESCRIPTION</span></span>
<span data-ttu-id="4e506-106">A **Remove-AzApplicationGatewaySslProfile** parancsmag eltávolítja az ssl-profilt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="4e506-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="4e506-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e506-107">EXAMPLES</span></span>

### <span data-ttu-id="4e506-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4e506-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="4e506-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="4e506-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="4e506-110">A második parancs eltávolítja az SslProfile01 nevű ssl-profilt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4e506-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4e506-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e506-111">PARAMETERS</span></span>

### <span data-ttu-id="4e506-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e506-112">-ApplicationGateway</span></span>
<span data-ttu-id="4e506-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e506-113">The applicationGateway</span></span>

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

### <span data-ttu-id="4e506-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e506-114">-DefaultProfile</span></span>
<span data-ttu-id="4e506-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e506-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e506-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4e506-116">-Name</span></span>
<span data-ttu-id="4e506-117">Az ssl-profil neve</span><span class="sxs-lookup"><span data-stu-id="4e506-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="4e506-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e506-118">CommonParameters</span></span>
<span data-ttu-id="4e506-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e506-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e506-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e506-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e506-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e506-121">INPUTS</span></span>

### <span data-ttu-id="4e506-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e506-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e506-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e506-123">OUTPUTS</span></span>

### <span data-ttu-id="4e506-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e506-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e506-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e506-125">NOTES</span></span>

## <span data-ttu-id="4e506-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e506-126">RELATED LINKS</span></span>

[<span data-ttu-id="4e506-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4e506-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="4e506-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4e506-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="4e506-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4e506-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="4e506-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4e506-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)