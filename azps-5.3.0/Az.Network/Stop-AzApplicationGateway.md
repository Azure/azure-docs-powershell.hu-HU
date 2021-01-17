---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479878"
---
# <span data-ttu-id="68ec3-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="68ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="68ec3-103">Alkalmazás-átjáró leállítja</span><span class="sxs-lookup"><span data-stu-id="68ec3-103">Stops an application gateway</span></span>

## <span data-ttu-id="68ec3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="68ec3-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68ec3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="68ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="68ec3-106">A **Stop-AzApplicationGateway** parancsmag leállít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="68ec3-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="68ec3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="68ec3-107">EXAMPLES</span></span>

### <span data-ttu-id="68ec3-108">1. példa: Alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="68ec3-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="68ec3-109">Ez a parancs leállítja a változóban tárolt $AppGw.</span><span class="sxs-lookup"><span data-stu-id="68ec3-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="68ec3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68ec3-110">PARAMETERS</span></span>

### <span data-ttu-id="68ec3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-111">-ApplicationGateway</span></span>
<span data-ttu-id="68ec3-112">Azt az alkalmazás-átjárót adja meg, amely a parancsmagot leállítja.</span><span class="sxs-lookup"><span data-stu-id="68ec3-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="68ec3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68ec3-113">-AsJob</span></span>
<span data-ttu-id="68ec3-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="68ec3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68ec3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ec3-115">-DefaultProfile</span></span>
<span data-ttu-id="68ec3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68ec3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68ec3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ec3-117">CommonParameters</span></span>
<span data-ttu-id="68ec3-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ec3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ec3-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ec3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ec3-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68ec3-120">INPUTS</span></span>

### <span data-ttu-id="68ec3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68ec3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68ec3-122">OUTPUTS</span></span>

### <span data-ttu-id="68ec3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68ec3-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="68ec3-124">NOTES</span></span>

## <span data-ttu-id="68ec3-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68ec3-125">RELATED LINKS</span></span>

[<span data-ttu-id="68ec3-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="68ec3-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="68ec3-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="68ec3-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="68ec3-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68ec3-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


