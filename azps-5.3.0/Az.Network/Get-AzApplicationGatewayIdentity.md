---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468205"
---
# <span data-ttu-id="3a37d-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="3a37d-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="3a37d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a37d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a37d-103">Identitás hozzárendelése az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3a37d-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="3a37d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a37d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a37d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a37d-105">DESCRIPTION</span></span>
<span data-ttu-id="3a37d-106">A **Get-AzApplicationGatewayIdentity** parancsmag identitást kap az alkalmazás-átjáróhoz rendelve.</span><span class="sxs-lookup"><span data-stu-id="3a37d-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="3a37d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a37d-107">EXAMPLES</span></span>

### <span data-ttu-id="3a37d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3a37d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="3a37d-109">Az alábbi példák azt mutatják be, hogy miként szerez be alkalmazás-átjáró identitást az Alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="3a37d-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="3a37d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a37d-110">PARAMETERS</span></span>

### <span data-ttu-id="3a37d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a37d-111">-ApplicationGateway</span></span>
<span data-ttu-id="3a37d-112">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a37d-112">The applicationGateway</span></span>

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

### <span data-ttu-id="3a37d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a37d-113">-DefaultProfile</span></span>
<span data-ttu-id="3a37d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a37d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a37d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a37d-115">CommonParameters</span></span>
<span data-ttu-id="3a37d-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a37d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a37d-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a37d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a37d-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a37d-118">INPUTS</span></span>

### <span data-ttu-id="3a37d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a37d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3a37d-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a37d-120">OUTPUTS</span></span>

### <span data-ttu-id="3a37d-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3a37d-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="3a37d-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a37d-122">NOTES</span></span>

## <span data-ttu-id="3a37d-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a37d-123">RELATED LINKS</span></span>
