---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347933"
---
# <span data-ttu-id="fd32f-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd32f-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="fd32f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd32f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd32f-103">Frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="fd32f-103">Updates an application gateway.</span></span>

## <span data-ttu-id="fd32f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd32f-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd32f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd32f-105">DESCRIPTION</span></span>
<span data-ttu-id="fd32f-106">A **Set-AzApplicationGateway** parancsmag frissíti az Azure-alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="fd32f-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="fd32f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd32f-107">EXAMPLES</span></span>

### <span data-ttu-id="fd32f-108">1. példa: Alkalmazás-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="fd32f-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="fd32f-109">Ezek a parancsok frissítik az alkalmazás átjáróját a $AppGw beállításokkal, és a frissített átjárót a $UpdatedAppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="fd32f-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="fd32f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd32f-110">PARAMETERS</span></span>

### <span data-ttu-id="fd32f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd32f-111">-ApplicationGateway</span></span>
<span data-ttu-id="fd32f-112">Egy olyan alkalmazás-átjáróobjektumot ad meg, amely az alkalmazás-átjáró beállításának állapotát jelzi.</span><span class="sxs-lookup"><span data-stu-id="fd32f-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="fd32f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd32f-113">-AsJob</span></span>
<span data-ttu-id="fd32f-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fd32f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd32f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd32f-115">-DefaultProfile</span></span>
<span data-ttu-id="fd32f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd32f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd32f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd32f-117">CommonParameters</span></span>
<span data-ttu-id="fd32f-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd32f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd32f-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd32f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd32f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd32f-120">INPUTS</span></span>

### <span data-ttu-id="fd32f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd32f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fd32f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd32f-122">OUTPUTS</span></span>

### <span data-ttu-id="fd32f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd32f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fd32f-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd32f-124">NOTES</span></span>

## <span data-ttu-id="fd32f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd32f-125">RELATED LINKS</span></span>

[<span data-ttu-id="fd32f-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd32f-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


