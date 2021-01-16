---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354161"
---
# <span data-ttu-id="2f9ae-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2f9ae-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="2f9ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9ae-103">Egy alkalmazás-átjáró háttér-HTTP-beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="2f9ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f9ae-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f9ae-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="2f9ae-106">A Get-AzApplicationGatewayBackendHttpSetting parancsmag egy alkalmazás-átjáró háttér-HTTP-beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="2f9ae-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="2f9ae-108">1. példa: Háttér-HTTP-beállítások kérése név szerint</span><span class="sxs-lookup"><span data-stu-id="2f9ae-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="2f9ae-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs a Beállítások01 NEVŰ HTTP-beállításokat kapja $AppGw a beállításokat a $Settings változóban.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="2f9ae-110">2. példa: Háttér-HTTP-beállítások gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="2f9ae-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="2f9ae-111">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs a http-beállítások gyűjteményét $AppGw és a beállításokat a $SettingsList tárolja.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="2f9ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f9ae-112">PARAMETERS</span></span>

### <span data-ttu-id="2f9ae-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f9ae-113">-ApplicationGateway</span></span>
<span data-ttu-id="2f9ae-114">Egy olyan alkalmazás-átjáróobjektumot ad meg, amely háttér-HTTP-beállításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="2f9ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f9ae-115">-DefaultProfile</span></span>
<span data-ttu-id="2f9ae-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f9ae-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2f9ae-117">-Name</span></span>
<span data-ttu-id="2f9ae-118">A parancsmag háttér-HTTP-beállításainak nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2f9ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9ae-119">CommonParameters</span></span>
<span data-ttu-id="2f9ae-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9ae-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f9ae-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9ae-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f9ae-122">INPUTS</span></span>

### <span data-ttu-id="2f9ae-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f9ae-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f9ae-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f9ae-124">OUTPUTS</span></span>

### <span data-ttu-id="2f9ae-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2f9ae-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2f9ae-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f9ae-126">NOTES</span></span>

## <span data-ttu-id="2f9ae-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f9ae-127">RELATED LINKS</span></span>

[<span data-ttu-id="2f9ae-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2f9ae-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2f9ae-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2f9ae-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2f9ae-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2f9ae-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2f9ae-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2f9ae-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

