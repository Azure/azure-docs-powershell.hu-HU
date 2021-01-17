---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340001"
---
# <span data-ttu-id="01455-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01455-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="01455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01455-102">SYNOPSIS</span></span>
<span data-ttu-id="01455-103">Új kapcsolatelvezetési konfigurációt hoz létre a háttér HTTP-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="01455-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="01455-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01455-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01455-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01455-105">DESCRIPTION</span></span>
<span data-ttu-id="01455-106">A **New-AzApplicationGatewayConnectionDraining** parancsmag új kapcsolatelvezetési konfigurációt hoz létre a háttér HTTP-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="01455-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="01455-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01455-107">EXAMPLES</span></span>

### <span data-ttu-id="01455-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="01455-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="01455-109">A parancs létrehoz egy új kapcsolatelvezetési konfigurációt, amelynél az Engedélyezett beállítás Igaz, az DrainTimeoutInSec pedig 42 másodpercre van állítva, és a beállítást $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="01455-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="01455-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01455-110">PARAMETERS</span></span>

### <span data-ttu-id="01455-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01455-111">-DefaultProfile</span></span>
<span data-ttu-id="01455-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01455-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01455-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="01455-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="01455-114">Aktív a kapcsolatelvezetés másodpercek alatt lefolyatva.</span><span class="sxs-lookup"><span data-stu-id="01455-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="01455-115">Az elfogadható értékek 1 másodperctől 3600 másodpercig esnek.</span><span class="sxs-lookup"><span data-stu-id="01455-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01455-116">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="01455-116">-Enabled</span></span>
<span data-ttu-id="01455-117">Hogy engedélyezve van-e a kapcsolat lemerülése.</span><span class="sxs-lookup"><span data-stu-id="01455-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01455-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01455-118">CommonParameters</span></span>
<span data-ttu-id="01455-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01455-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01455-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01455-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01455-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01455-121">INPUTS</span></span>

### <span data-ttu-id="01455-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="01455-122">None</span></span>

## <span data-ttu-id="01455-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01455-123">OUTPUTS</span></span>

### <span data-ttu-id="01455-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01455-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="01455-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01455-125">NOTES</span></span>

## <span data-ttu-id="01455-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01455-126">RELATED LINKS</span></span>

[<span data-ttu-id="01455-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01455-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="01455-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01455-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="01455-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01455-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

