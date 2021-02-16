---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 238c5974871379a3552d6b0d23b696bb513dc21f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415104"
---
# <span data-ttu-id="62c0e-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62c0e-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="62c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="62c0e-103">Módosítja a háttér HTTP-beállítások objektum kapcsolatelvezetési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="62c0e-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="62c0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62c0e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c0e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="62c0e-106">A **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag módosítja a háttér HTTP-beállítási objektum kapcsolatleerítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="62c0e-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="62c0e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62c0e-107">EXAMPLES</span></span>

### <span data-ttu-id="62c0e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="62c0e-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="62c0e-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="62c0e-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="62c0e-110">A második parancs a Beállítások01 nevű háttér-HTTP-beállításokat kapja $AppGw és a beállításokat a $Settings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="62c0e-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="62c0e-111">Az utolsó parancs módosítja az $Settings-ben tárolt háttér HTTP-beállítások objektum kapcsolatelvezetési konfigurációját úgy, hogy az Engedélyezve a Hamis, az DrainTimeoutInSec beállítást pedig 3600-ra módosítja.</span><span class="sxs-lookup"><span data-stu-id="62c0e-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="62c0e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62c0e-112">PARAMETERS</span></span>

### <span data-ttu-id="62c0e-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="62c0e-113">-BackendHttpSettings</span></span>
<span data-ttu-id="62c0e-114">A háttér http-beállításai</span><span class="sxs-lookup"><span data-stu-id="62c0e-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62c0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c0e-115">-DefaultProfile</span></span>
<span data-ttu-id="62c0e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62c0e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c0e-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="62c0e-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="62c0e-118">Aktív a kapcsolatelvezetés másodpercek alatt lefolyatva.</span><span class="sxs-lookup"><span data-stu-id="62c0e-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="62c0e-119">Az elfogadható értékek 1 másodperctől 3600 másodpercig esnek.</span><span class="sxs-lookup"><span data-stu-id="62c0e-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="62c0e-120">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="62c0e-120">-Enabled</span></span>
<span data-ttu-id="62c0e-121">Hogy engedélyezve van-e a kapcsolat lemerülése.</span><span class="sxs-lookup"><span data-stu-id="62c0e-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="62c0e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c0e-122">CommonParameters</span></span>
<span data-ttu-id="62c0e-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c0e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c0e-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c0e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c0e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62c0e-125">INPUTS</span></span>

### <span data-ttu-id="62c0e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="62c0e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="62c0e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c0e-127">OUTPUTS</span></span>

### <span data-ttu-id="62c0e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="62c0e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="62c0e-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62c0e-129">NOTES</span></span>

## <span data-ttu-id="62c0e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62c0e-130">RELATED LINKS</span></span>

[<span data-ttu-id="62c0e-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62c0e-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="62c0e-132">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62c0e-132">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="62c0e-133">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62c0e-133">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="62c0e-134">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62c0e-134">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

