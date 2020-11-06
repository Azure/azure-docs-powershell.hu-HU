---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: d7dc38e25ffda43eae3c29bc0e3db83f1a27c9f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495086"
---
# <span data-ttu-id="ba89a-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba89a-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ba89a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba89a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba89a-103">Az alkalmazás-átjárók back-end HTTP-beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba89a-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba89a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba89a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba89a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba89a-105">DESCRIPTION</span></span>
<span data-ttu-id="ba89a-106">A Get-AzureRmApplicationGatewayBackendHttpSettings parancsmag az alkalmazás-átjárók back-end HTTP-beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba89a-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="ba89a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba89a-107">EXAMPLES</span></span>

### <span data-ttu-id="ba89a-108">Példa 1: a HTTP-beállítások visszaszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="ba89a-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ba89a-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs beolvassa a Settings01 $AppGw nevű HTTP-beállításokat, és az $Settings változóban tárolja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="ba89a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="ba89a-110">2. példa: a back-end HTTP-beállítások gyűjteményének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ba89a-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="ba89a-111">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs beolvassa a $AppGw HTTP-beállításainak gyűjteményét, és a beállításokat a $SettingsList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba89a-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="ba89a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba89a-112">PARAMETERS</span></span>

### <span data-ttu-id="ba89a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba89a-113">-ApplicationGateway</span></span>
<span data-ttu-id="ba89a-114">Egy olyan Application Gateway-objektumot ad meg, amely a végfelhasználói HTTP-beállításokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ba89a-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="ba89a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba89a-115">-DefaultProfile</span></span>
<span data-ttu-id="ba89a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba89a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba89a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba89a-117">-Name</span></span>
<span data-ttu-id="ba89a-118">Annak a backend-HTTP-beállításoknak a neve, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="ba89a-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba89a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba89a-119">CommonParameters</span></span>
<span data-ttu-id="ba89a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba89a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba89a-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba89a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba89a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba89a-122">INPUTS</span></span>

### <span data-ttu-id="ba89a-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba89a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ba89a-124">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba89a-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ba89a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba89a-125">OUTPUTS</span></span>

### <span data-ttu-id="ba89a-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba89a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ba89a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba89a-127">NOTES</span></span>

## <span data-ttu-id="ba89a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba89a-128">RELATED LINKS</span></span>

[<span data-ttu-id="ba89a-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba89a-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="ba89a-130">Új – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba89a-130">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="ba89a-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba89a-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="ba89a-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba89a-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

