---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157114"
---
# <span data-ttu-id="3ce45-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="3ce45-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="3ce45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce45-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce45-103">Az Ssl-házirend összes elérhető ssl-beállítását beveszi az Alkalmazásátjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3ce45-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="3ce45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ce45-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce45-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ce45-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce45-106">A **Get-AzApplicationGatewayAvailableSslOption parancsmag** az ssl-házirend összes elérhető ssl-beállítását megkapja</span><span class="sxs-lookup"><span data-stu-id="3ce45-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="3ce45-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ce45-107">EXAMPLES</span></span>

### <span data-ttu-id="3ce45-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3ce45-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="3ce45-109">Ez a parancs az ssl-házirend összes elérhető ssl-beállítását visszaadja.</span><span class="sxs-lookup"><span data-stu-id="3ce45-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="3ce45-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ce45-110">PARAMETERS</span></span>

### <span data-ttu-id="3ce45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce45-111">-DefaultProfile</span></span>
<span data-ttu-id="3ce45-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ce45-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ce45-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce45-113">CommonParameters</span></span>
<span data-ttu-id="3ce45-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce45-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce45-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ce45-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce45-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ce45-116">INPUTS</span></span>

### <span data-ttu-id="3ce45-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="3ce45-117">None</span></span>

## <span data-ttu-id="3ce45-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ce45-118">OUTPUTS</span></span>

### <span data-ttu-id="3ce45-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="3ce45-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="3ce45-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ce45-120">NOTES</span></span>

## <span data-ttu-id="3ce45-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ce45-121">RELATED LINKS</span></span>
