---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837047"
---
# <span data-ttu-id="7c125-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7c125-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="7c125-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c125-102">SYNOPSIS</span></span>
<span data-ttu-id="7c125-103">Az alkalmazás-átjárók tűzfal-házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="7c125-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="7c125-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c125-104">SYNTAX</span></span>

### <span data-ttu-id="7c125-105">ByFactoryObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c125-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c125-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="7c125-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c125-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c125-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c125-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c125-108">DESCRIPTION</span></span>
<span data-ttu-id="7c125-109">A **set-AzApplicationGatewayFirewallPolicy** parancsmag egy Azure Application gateway tűzfal-házirendet frissít.</span><span class="sxs-lookup"><span data-stu-id="7c125-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="7c125-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7c125-110">EXAMPLES</span></span>

### <span data-ttu-id="7c125-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c125-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="7c125-112">Ez a parancs frissíti az alkalmazás-átjáró tűzfal-házirendjét a $AppGwFirewallPolicy változó beállításaival, és a $UpdatedAppGwFirewallPolicy változóban tárolja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="7c125-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="7c125-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c125-113">PARAMETERS</span></span>

### <span data-ttu-id="7c125-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c125-114">-AsJob</span></span>
<span data-ttu-id="7c125-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7c125-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c125-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="7c125-116">-CustomRule</span></span>
<span data-ttu-id="7c125-117">A CustomRules listája</span><span class="sxs-lookup"><span data-stu-id="7c125-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c125-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c125-118">-DefaultProfile</span></span>
<span data-ttu-id="7c125-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c125-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c125-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c125-120">-InputObject</span></span>
<span data-ttu-id="7c125-121">A applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7c125-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c125-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c125-122">-Name</span></span>
<span data-ttu-id="7c125-123">A tűzfal házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="7c125-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c125-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c125-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c125-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c125-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c125-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c125-126">-ResourceId</span></span>
<span data-ttu-id="7c125-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="7c125-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c125-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c125-128">CommonParameters</span></span>
<span data-ttu-id="7c125-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c125-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c125-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c125-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c125-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c125-131">INPUTS</span></span>

### <span data-ttu-id="7c125-132">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7c125-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="7c125-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c125-133">OUTPUTS</span></span>

### <span data-ttu-id="7c125-134">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7c125-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="7c125-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c125-135">NOTES</span></span>

## <span data-ttu-id="7c125-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c125-136">RELATED LINKS</span></span>
