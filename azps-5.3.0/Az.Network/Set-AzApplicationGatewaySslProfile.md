---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479942"
---
# <span data-ttu-id="07624-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07624-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="07624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07624-102">SYNOPSIS</span></span>
<span data-ttu-id="07624-103">Frissíti egy alkalmazás-átjáró ssl-profilját.</span><span class="sxs-lookup"><span data-stu-id="07624-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="07624-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07624-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07624-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07624-105">DESCRIPTION</span></span>
<span data-ttu-id="07624-106">A **Set-AzApplicationGatewaySslProfile** parancsmag frissíti egy Azure-alkalmazás átjáró ssl-profilját.</span><span class="sxs-lookup"><span data-stu-id="07624-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="07624-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07624-107">EXAMPLES</span></span>

### <span data-ttu-id="07624-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="07624-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="07624-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="07624-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="07624-110">A második parancs frissíti az alkalmazás átjárójának ssl-profilját a $AppGw változóban, és frissíti az ügyfél-hitelesítés konfigurációját a $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="07624-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="07624-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07624-111">PARAMETERS</span></span>

### <span data-ttu-id="07624-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07624-112">-ApplicationGateway</span></span>
<span data-ttu-id="07624-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="07624-113">The applicationGateway</span></span>

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

### <span data-ttu-id="07624-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="07624-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="07624-115">Ügyfél-hitelesítés konfigurációs beállításai</span><span class="sxs-lookup"><span data-stu-id="07624-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07624-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07624-116">-DefaultProfile</span></span>
<span data-ttu-id="07624-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07624-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07624-118">-Name</span><span class="sxs-lookup"><span data-stu-id="07624-118">-Name</span></span>
<span data-ttu-id="07624-119">Az SSL-profil neve</span><span class="sxs-lookup"><span data-stu-id="07624-119">The name of the SSL profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07624-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="07624-120">-SslPolicy</span></span>
<span data-ttu-id="07624-121">SSL-házirend</span><span class="sxs-lookup"><span data-stu-id="07624-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07624-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="07624-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="07624-123">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncai</span><span class="sxs-lookup"><span data-stu-id="07624-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07624-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07624-124">CommonParameters</span></span>
<span data-ttu-id="07624-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07624-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07624-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07624-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07624-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07624-127">INPUTS</span></span>

### <span data-ttu-id="07624-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07624-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07624-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07624-129">OUTPUTS</span></span>

### <span data-ttu-id="07624-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07624-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07624-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07624-131">NOTES</span></span>

## <span data-ttu-id="07624-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07624-132">RELATED LINKS</span></span>

[<span data-ttu-id="07624-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07624-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="07624-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07624-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="07624-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07624-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="07624-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07624-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)