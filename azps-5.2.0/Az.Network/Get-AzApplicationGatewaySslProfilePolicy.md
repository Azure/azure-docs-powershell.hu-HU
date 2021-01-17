---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337854"
---
# <span data-ttu-id="2a4a1-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a4a1-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="2a4a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4a1-103">Egy alkalmazás-átjáró SSL-profiljának SSL-házirendét használja.</span><span class="sxs-lookup"><span data-stu-id="2a4a1-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="2a4a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a4a1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a4a1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a4a1-105">DESCRIPTION</span></span>
<span data-ttu-id="2a4a1-106">A **Get-AzApplicationGatewaySslProfilePolicy** parancsmag egy alkalmazás-átjáró SSL-profiljának SSL-házirendjére érvényes.</span><span class="sxs-lookup"><span data-stu-id="2a4a1-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="2a4a1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a4a1-107">EXAMPLES</span></span>

### <span data-ttu-id="2a4a1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2a4a1-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="2a4a1-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="2a4a1-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="2a4a1-110">A második parancs az SslProfile01 nevű SSL-profilt kapja meg a $AppGw, és azt $SslProfile tárolja.</span><span class="sxs-lookup"><span data-stu-id="2a4a1-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="2a4a1-111">Az utolsó parancs az SSL-profilból kapja meg az SSL$SslProfile és tárolja azt a $sslpolicy változóban.</span><span class="sxs-lookup"><span data-stu-id="2a4a1-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="2a4a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a4a1-112">PARAMETERS</span></span>

### <span data-ttu-id="2a4a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4a1-113">-DefaultProfile</span></span>
<span data-ttu-id="2a4a1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a4a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a4a1-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="2a4a1-115">-SslProfile</span></span>
<span data-ttu-id="2a4a1-116">Az alkalmazás átjáró ssl-profilja</span><span class="sxs-lookup"><span data-stu-id="2a4a1-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="2a4a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4a1-117">CommonParameters</span></span>
<span data-ttu-id="2a4a1-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a4a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4a1-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a4a1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4a1-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a4a1-120">INPUTS</span></span>

### <span data-ttu-id="2a4a1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2a4a1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2a4a1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a4a1-122">OUTPUTS</span></span>

### <span data-ttu-id="2a4a1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2a4a1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="2a4a1-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a4a1-124">NOTES</span></span>

## <span data-ttu-id="2a4a1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a4a1-125">RELATED LINKS</span></span>

[<span data-ttu-id="2a4a1-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a4a1-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="2a4a1-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a4a1-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="2a4a1-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a4a1-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="2a4a1-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="2a4a1-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)