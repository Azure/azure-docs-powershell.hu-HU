---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363480"
---
# <span data-ttu-id="b359a-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="b359a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b359a-102">SYNOPSIS</span></span>
<span data-ttu-id="b359a-103">Alkalmazás-átjáró leállítja</span><span class="sxs-lookup"><span data-stu-id="b359a-103">Stops an application gateway</span></span>

## <span data-ttu-id="b359a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b359a-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b359a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b359a-105">DESCRIPTION</span></span>
<span data-ttu-id="b359a-106">A **Stop-AzApplicationGateway** parancsmag leállít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="b359a-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="b359a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b359a-107">EXAMPLES</span></span>

### <span data-ttu-id="b359a-108">1. példa: Alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="b359a-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b359a-109">Ez a parancs leállítja a változóban tárolt $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="b359a-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="b359a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b359a-110">PARAMETERS</span></span>

### <span data-ttu-id="b359a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-111">-ApplicationGateway</span></span>
<span data-ttu-id="b359a-112">Azt az alkalmazás-átjárót adja meg, amely a parancsmagot leállítja.</span><span class="sxs-lookup"><span data-stu-id="b359a-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b359a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b359a-113">-AsJob</span></span>
<span data-ttu-id="b359a-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b359a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b359a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b359a-115">-DefaultProfile</span></span>
<span data-ttu-id="b359a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b359a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b359a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b359a-117">CommonParameters</span></span>
<span data-ttu-id="b359a-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b359a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b359a-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b359a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b359a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b359a-120">INPUTS</span></span>

### <span data-ttu-id="b359a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b359a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b359a-122">OUTPUTS</span></span>

### <span data-ttu-id="b359a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b359a-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b359a-124">NOTES</span></span>

## <span data-ttu-id="b359a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b359a-125">RELATED LINKS</span></span>

[<span data-ttu-id="b359a-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b359a-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="b359a-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="b359a-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="b359a-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b359a-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


