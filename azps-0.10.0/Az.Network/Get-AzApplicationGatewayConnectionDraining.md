---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 842ac402becd78decb00333c39a4a8247d543987
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841733"
---
# <span data-ttu-id="9145d-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9145d-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9145d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9145d-102">SYNOPSIS</span></span>
<span data-ttu-id="9145d-103">A back-end HTTP Settings objektum kapcsolat-ürítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9145d-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9145d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9145d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9145d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9145d-105">DESCRIPTION</span></span>
<span data-ttu-id="9145d-106">A **Get-AzApplicationGatewayConnectionDraining** parancsmag a back-end http Settings objektum kapcsolat-kiürítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9145d-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9145d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9145d-107">EXAMPLES</span></span>

### <span data-ttu-id="9145d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9145d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="9145d-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9145d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9145d-110">A második parancs megkapja a Settings01 $AppGw nevű back-end HTTP-beállításokat, és a $Settings változó beállításait tárolja.</span><span class="sxs-lookup"><span data-stu-id="9145d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="9145d-111">Az utolsó parancs a kapcsolat-levezetési konfigurációt kapja a back-end HTTP-beállításokból $Settings és a $ConnectionDraining változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9145d-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="9145d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9145d-112">PARAMETERS</span></span>

### <span data-ttu-id="9145d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9145d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="9145d-114">A backend http-beállításai</span><span class="sxs-lookup"><span data-stu-id="9145d-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9145d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9145d-115">-DefaultProfile</span></span>
<span data-ttu-id="9145d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9145d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9145d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9145d-117">CommonParameters</span></span>
<span data-ttu-id="9145d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9145d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9145d-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9145d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9145d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9145d-120">INPUTS</span></span>

### <span data-ttu-id="9145d-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9145d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9145d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9145d-122">OUTPUTS</span></span>

### <span data-ttu-id="9145d-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9145d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9145d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9145d-124">NOTES</span></span>

## <span data-ttu-id="9145d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9145d-125">RELATED LINKS</span></span>

[<span data-ttu-id="9145d-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9145d-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="9145d-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9145d-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9145d-128">Új – AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9145d-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9145d-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9145d-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9145d-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9145d-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
