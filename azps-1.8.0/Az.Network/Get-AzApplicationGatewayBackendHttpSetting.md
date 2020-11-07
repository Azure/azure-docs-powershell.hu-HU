---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 0261eb6ed3a88ca33edce134911c405f530a2a5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670662"
---
# <span data-ttu-id="7c040-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7c040-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="7c040-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c040-102">SYNOPSIS</span></span>
<span data-ttu-id="7c040-103">Az alkalmazás-átjárók back-end HTTP-beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7c040-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="7c040-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c040-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c040-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c040-105">DESCRIPTION</span></span>
<span data-ttu-id="7c040-106">A Get-AzApplicationGatewayBackendHttpSetting parancsmag az alkalmazás-átjárók back-end HTTP-beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7c040-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="7c040-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c040-107">EXAMPLES</span></span>

### <span data-ttu-id="7c040-108">Példa 1: a HTTP-beállítások visszaszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="7c040-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7c040-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs beolvassa a Settings01 $AppGw nevű HTTP-beállításokat, és az $Settings változóban tárolja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="7c040-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="7c040-110">2. példa: a back-end HTTP-beállítások gyűjteményének beszerzése</span><span class="sxs-lookup"><span data-stu-id="7c040-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="7c040-111">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs beolvassa a $AppGw HTTP-beállításainak gyűjteményét, és a beállításokat a $SettingsList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7c040-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="7c040-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c040-112">PARAMETERS</span></span>

### <span data-ttu-id="7c040-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c040-113">-ApplicationGateway</span></span>
<span data-ttu-id="7c040-114">Egy olyan Application Gateway-objektumot ad meg, amely a végfelhasználói HTTP-beállításokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7c040-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="7c040-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c040-115">-DefaultProfile</span></span>
<span data-ttu-id="7c040-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c040-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c040-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c040-117">-Name</span></span>
<span data-ttu-id="7c040-118">Annak a backend-HTTP-beállításoknak a neve, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="7c040-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7c040-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c040-119">CommonParameters</span></span>
<span data-ttu-id="7c040-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c040-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c040-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c040-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c040-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c040-122">INPUTS</span></span>

### <span data-ttu-id="7c040-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c040-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7c040-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c040-124">OUTPUTS</span></span>

### <span data-ttu-id="7c040-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7c040-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7c040-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c040-126">NOTES</span></span>

## <span data-ttu-id="7c040-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c040-127">RELATED LINKS</span></span>

[<span data-ttu-id="7c040-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7c040-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7c040-129">Új – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7c040-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7c040-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7c040-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7c040-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7c040-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

