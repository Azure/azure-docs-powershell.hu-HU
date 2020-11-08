---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195705"
---
# <span data-ttu-id="2e46f-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e46f-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="2e46f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e46f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e46f-103">Az alkalmazás-átjáró privát hivatkozásának beállítása.</span><span class="sxs-lookup"><span data-stu-id="2e46f-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="2e46f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e46f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e46f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e46f-105">DESCRIPTION</span></span>
<span data-ttu-id="2e46f-106">A **Get-AzApplicationGatewayPrivateLinkConfiguration** parancsmag az Application Gateway privát hivatkozásának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2e46f-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="2e46f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e46f-107">EXAMPLES</span></span>

### <span data-ttu-id="2e46f-108">Példa 1: a privát hivatkozás beszerzése beállítás</span><span class="sxs-lookup"><span data-stu-id="2e46f-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="2e46f-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2e46f-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2e46f-110">A második parancs beolvassa a privateLinkConfig01 nevű privát hivatkozás-konfigurációt a $AppGw, és a $PrivateLinkConfiguration változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2e46f-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="2e46f-111">2. példa: a privát hivatkozás konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2e46f-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="2e46f-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2e46f-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2e46f-113">A második parancs a $AppGw, és a $PrivateLinkConfigurations változóban tárolja az összes magánjellegű hivatkozás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2e46f-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="2e46f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e46f-114">PARAMETERS</span></span>

### <span data-ttu-id="2e46f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e46f-115">-ApplicationGateway</span></span>
<span data-ttu-id="2e46f-116">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e46f-116">The applicationGateway</span></span>

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

### <span data-ttu-id="2e46f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e46f-117">-DefaultProfile</span></span>
<span data-ttu-id="2e46f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e46f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e46f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e46f-119">-Name</span></span>
<span data-ttu-id="2e46f-120">Az Application Gateway privateLink-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="2e46f-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="2e46f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e46f-121">CommonParameters</span></span>
<span data-ttu-id="2e46f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e46f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e46f-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e46f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e46f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e46f-124">INPUTS</span></span>

### <span data-ttu-id="2e46f-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e46f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2e46f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e46f-126">OUTPUTS</span></span>

### <span data-ttu-id="2e46f-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e46f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="2e46f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e46f-128">NOTES</span></span>

## <span data-ttu-id="2e46f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e46f-129">RELATED LINKS</span></span>

[<span data-ttu-id="2e46f-130">Új – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e46f-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2e46f-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e46f-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2e46f-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e46f-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2e46f-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e46f-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)