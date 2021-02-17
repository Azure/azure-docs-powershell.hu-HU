---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206990"
---
# <span data-ttu-id="1e453-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="1e453-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="1e453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e453-102">SYNOPSIS</span></span>
<span data-ttu-id="1e453-103">Identitás hozzárendelése az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="1e453-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="1e453-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e453-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e453-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e453-105">DESCRIPTION</span></span>
<span data-ttu-id="1e453-106">A **Get-AzApplicationGatewayIdentity** parancsmag identitást kap az alkalmazás-átjáróhoz rendelve.</span><span class="sxs-lookup"><span data-stu-id="1e453-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="1e453-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e453-107">EXAMPLES</span></span>

### <span data-ttu-id="1e453-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1e453-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="1e453-109">Az alábbi példák azt mutatják be, hogy miként szerez be alkalmazás-átjáró identitást az Alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="1e453-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="1e453-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e453-110">PARAMETERS</span></span>

### <span data-ttu-id="1e453-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e453-111">-ApplicationGateway</span></span>
<span data-ttu-id="1e453-112">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e453-112">The applicationGateway</span></span>

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

### <span data-ttu-id="1e453-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e453-113">-DefaultProfile</span></span>
<span data-ttu-id="1e453-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e453-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e453-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e453-115">CommonParameters</span></span>
<span data-ttu-id="1e453-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e453-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e453-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e453-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e453-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e453-118">INPUTS</span></span>

### <span data-ttu-id="1e453-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e453-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e453-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e453-120">OUTPUTS</span></span>

### <span data-ttu-id="1e453-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1e453-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="1e453-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e453-122">NOTES</span></span>

## <span data-ttu-id="1e453-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e453-123">RELATED LINKS</span></span>
