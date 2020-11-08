---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182506"
---
# <span data-ttu-id="f1657-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1657-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="f1657-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1657-102">SYNOPSIS</span></span>
<span data-ttu-id="f1657-103">Az alkalmazás-átjáró privát hivatkozásának beállítása.</span><span class="sxs-lookup"><span data-stu-id="f1657-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="f1657-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1657-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1657-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1657-105">DESCRIPTION</span></span>
<span data-ttu-id="f1657-106">A **Get-AzApplicationGatewayPrivateLinkConfiguration** parancsmag az Application Gateway privát hivatkozásának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f1657-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="f1657-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1657-107">EXAMPLES</span></span>

### <span data-ttu-id="f1657-108">Példa 1: a privát hivatkozás beszerzése beállítás</span><span class="sxs-lookup"><span data-stu-id="f1657-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="f1657-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f1657-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f1657-110">A második parancs beolvassa a privateLinkConfig01 nevű privát hivatkozás-konfigurációt a $AppGw, és a $PrivateLinkConfiguration változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f1657-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="f1657-111">2. példa: a privát hivatkozás konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f1657-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="f1657-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f1657-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f1657-113">A második parancs a $AppGw, és a $PrivateLinkConfigurations változóban tárolja az összes magánjellegű hivatkozás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f1657-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="f1657-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1657-114">PARAMETERS</span></span>

### <span data-ttu-id="f1657-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1657-115">-ApplicationGateway</span></span>
<span data-ttu-id="f1657-116">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1657-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1657-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1657-117">-DefaultProfile</span></span>
<span data-ttu-id="f1657-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1657-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1657-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1657-119">-Name</span></span>
<span data-ttu-id="f1657-120">Az Application Gateway privateLink-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="f1657-120">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1657-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1657-121">CommonParameters</span></span>
<span data-ttu-id="f1657-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1657-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1657-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1657-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1657-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1657-124">INPUTS</span></span>

### <span data-ttu-id="f1657-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1657-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1657-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1657-126">OUTPUTS</span></span>

### <span data-ttu-id="f1657-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1657-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="f1657-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1657-128">NOTES</span></span>

## <span data-ttu-id="f1657-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1657-129">RELATED LINKS</span></span>

[<span data-ttu-id="f1657-130">Új – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1657-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="f1657-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1657-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="f1657-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1657-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="f1657-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1657-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)