---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 88a89a17adc7a05e75865121d2133f723e534fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922762"
---
# <span data-ttu-id="60eb5-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="60eb5-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="60eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="60eb5-103">Eltávolít egy SSL-házirendet egy Azure alkalmazás-átjáró SSL-profiljából.</span><span class="sxs-lookup"><span data-stu-id="60eb5-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="60eb5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60eb5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60eb5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="60eb5-106">A Remove-AzApplicationGatewaySslProfilePolicy parancsmag eltávolítja az SSL-házirendet egy Azure-alkalmazás átjáró SSL-profilból.</span><span class="sxs-lookup"><span data-stu-id="60eb5-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="60eb5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60eb5-107">EXAMPLES</span></span>

### <span data-ttu-id="60eb5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="60eb5-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="60eb5-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="60eb5-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="60eb5-110">A második parancs a Profil01 nevű SSL-profilt kapja $AppGw és tárolja a $profile változóban.</span><span class="sxs-lookup"><span data-stu-id="60eb5-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="60eb5-111">Az utolsó parancs eltávolítja az ssl-profil ssl-házirendet a $profile.</span><span class="sxs-lookup"><span data-stu-id="60eb5-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="60eb5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60eb5-112">PARAMETERS</span></span>

### <span data-ttu-id="60eb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60eb5-113">-DefaultProfile</span></span>
<span data-ttu-id="60eb5-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60eb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60eb5-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="60eb5-115">-SslProfile</span></span>
<span data-ttu-id="60eb5-116">Az applicationGateway SSL-profil</span><span class="sxs-lookup"><span data-stu-id="60eb5-116">The applicationGateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60eb5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60eb5-117">-Confirm</span></span>
<span data-ttu-id="60eb5-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="60eb5-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60eb5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60eb5-119">-WhatIf</span></span>
<span data-ttu-id="60eb5-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="60eb5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60eb5-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60eb5-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60eb5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60eb5-122">CommonParameters</span></span>
<span data-ttu-id="60eb5-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60eb5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60eb5-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60eb5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60eb5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60eb5-125">INPUTS</span></span>

### <span data-ttu-id="60eb5-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="60eb5-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="60eb5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60eb5-127">OUTPUTS</span></span>

### <span data-ttu-id="60eb5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="60eb5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="60eb5-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60eb5-129">NOTES</span></span>

## <span data-ttu-id="60eb5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60eb5-130">RELATED LINKS</span></span>

[<span data-ttu-id="60eb5-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="60eb5-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="60eb5-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="60eb5-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="60eb5-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="60eb5-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="60eb5-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="60eb5-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)