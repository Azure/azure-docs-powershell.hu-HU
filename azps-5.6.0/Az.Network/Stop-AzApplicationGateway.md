---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 0cf179bf02c8590bd5c5e30277c7299c7b13b06b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918546"
---
# <span data-ttu-id="47093-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="47093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47093-102">SYNOPSIS</span></span>
<span data-ttu-id="47093-103">Alkalmazás-átjáró leállítja</span><span class="sxs-lookup"><span data-stu-id="47093-103">Stops an application gateway</span></span>

## <span data-ttu-id="47093-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47093-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47093-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47093-105">DESCRIPTION</span></span>
<span data-ttu-id="47093-106">A **Stop-AzApplicationGateway** parancsmag leállít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="47093-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="47093-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47093-107">EXAMPLES</span></span>

### <span data-ttu-id="47093-108">1. példa: Alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="47093-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="47093-109">Ez a parancs leállítja a változóban tárolt $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="47093-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="47093-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47093-110">PARAMETERS</span></span>

### <span data-ttu-id="47093-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-111">-ApplicationGateway</span></span>
<span data-ttu-id="47093-112">Azt az alkalmazás-átjárót adja meg, amely a parancsmagot leállítja.</span><span class="sxs-lookup"><span data-stu-id="47093-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="47093-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47093-113">-AsJob</span></span>
<span data-ttu-id="47093-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="47093-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47093-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47093-115">-DefaultProfile</span></span>
<span data-ttu-id="47093-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47093-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47093-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47093-117">CommonParameters</span></span>
<span data-ttu-id="47093-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47093-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47093-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47093-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47093-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47093-120">INPUTS</span></span>

### <span data-ttu-id="47093-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47093-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47093-122">OUTPUTS</span></span>

### <span data-ttu-id="47093-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47093-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47093-124">NOTES</span></span>

## <span data-ttu-id="47093-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47093-125">RELATED LINKS</span></span>

[<span data-ttu-id="47093-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="47093-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="47093-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="47093-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="47093-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47093-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


