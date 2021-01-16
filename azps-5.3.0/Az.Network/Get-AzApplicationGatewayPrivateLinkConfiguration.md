---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468206"
---
# <span data-ttu-id="591aa-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="591aa-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="591aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591aa-102">SYNOPSIS</span></span>
<span data-ttu-id="591aa-103">Egy alkalmazás átjárójának magánjellegű csatolás-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="591aa-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="591aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="591aa-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="591aa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="591aa-105">DESCRIPTION</span></span>
<span data-ttu-id="591aa-106">A **Get-AzApplicationGatewayPrivateLinkConfiguration** parancsmag az alkalmazás-átjárók privát csatolási konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="591aa-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="591aa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="591aa-107">EXAMPLES</span></span>

### <span data-ttu-id="591aa-108">1. példa: Megadott privát hivatkozáskonfiguráció beállítása</span><span class="sxs-lookup"><span data-stu-id="591aa-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="591aa-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="591aa-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="591aa-110">A második parancs a privateLinkConfig01 nevű privát hivatkozáskonfigurációt $AppGw és tárolja a $PrivateLinkConfiguration változóban.</span><span class="sxs-lookup"><span data-stu-id="591aa-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="591aa-111">2. példa: A privát hivatkozáskonfiguráció listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="591aa-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="591aa-112">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="591aa-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="591aa-113">A második parancs az összes privát hivatkozáskonfigurációt $AppGw a $PrivateLinkConfigurations tárolja.</span><span class="sxs-lookup"><span data-stu-id="591aa-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="591aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="591aa-114">PARAMETERS</span></span>

### <span data-ttu-id="591aa-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="591aa-115">-ApplicationGateway</span></span>
<span data-ttu-id="591aa-116">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="591aa-116">The applicationGateway</span></span>

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

### <span data-ttu-id="591aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-117">-DefaultProfile</span></span>
<span data-ttu-id="591aa-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="591aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="591aa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="591aa-119">-Name</span></span>
<span data-ttu-id="591aa-120">Az alkalmazás átjárójának privateLink-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="591aa-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="591aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591aa-121">CommonParameters</span></span>
<span data-ttu-id="591aa-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591aa-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="591aa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591aa-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="591aa-124">INPUTS</span></span>

### <span data-ttu-id="591aa-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="591aa-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="591aa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="591aa-126">OUTPUTS</span></span>

### <span data-ttu-id="591aa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="591aa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="591aa-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="591aa-128">NOTES</span></span>

## <span data-ttu-id="591aa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="591aa-129">RELATED LINKS</span></span>

[<span data-ttu-id="591aa-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="591aa-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="591aa-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="591aa-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="591aa-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="591aa-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="591aa-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="591aa-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)