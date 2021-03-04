---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e6b9c873110118392e9380418276bfa0f4d938a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933466"
---
# <span data-ttu-id="5673c-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5673c-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="5673c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5673c-102">SYNOPSIS</span></span>
<span data-ttu-id="5673c-103">Frissíti az alkalmazás átjáró tűzfal házirendet.</span><span class="sxs-lookup"><span data-stu-id="5673c-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="5673c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5673c-104">SYNTAX</span></span>

### <span data-ttu-id="5673c-105">ByFactoryObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5673c-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5673c-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="5673c-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5673c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5673c-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5673c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5673c-108">DESCRIPTION</span></span>
<span data-ttu-id="5673c-109">A **Set-AzApplicationGatewayFirewallPolicy parancsmag** frissíti az Azure-alkalmazás átjáró tűzfalházira vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="5673c-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="5673c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5673c-110">EXAMPLES</span></span>

### <span data-ttu-id="5673c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5673c-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="5673c-112">Ez a parancs frissíti az alkalmazás átjáró tűzfal házirendját a $AppGwFirewallPolicy beállításokkal, és a frissített átjárót a $UpdatedAppGwFirewallPolicy tárolja.</span><span class="sxs-lookup"><span data-stu-id="5673c-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="5673c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5673c-113">PARAMETERS</span></span>

### <span data-ttu-id="5673c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5673c-114">-AsJob</span></span>
<span data-ttu-id="5673c-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5673c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5673c-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="5673c-116">-CustomRule</span></span>
<span data-ttu-id="5673c-117">The list of CustomRules</span><span class="sxs-lookup"><span data-stu-id="5673c-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="5673c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5673c-118">-DefaultProfile</span></span>
<span data-ttu-id="5673c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5673c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5673c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5673c-120">-InputObject</span></span>
<span data-ttu-id="5673c-121">The applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5673c-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="5673c-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5673c-122">-ManagedRule</span></span>
<span data-ttu-id="5673c-123">A tűzfal házirend Felügyeltszabályai</span><span class="sxs-lookup"><span data-stu-id="5673c-123">ManagedRules of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5673c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5673c-124">-Name</span></span>
<span data-ttu-id="5673c-125">A tűzfal házirendneve.</span><span class="sxs-lookup"><span data-stu-id="5673c-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="5673c-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="5673c-126">-PolicySetting</span></span>
<span data-ttu-id="5673c-127">A tűzfal házirend házirend-beállításai</span><span class="sxs-lookup"><span data-stu-id="5673c-127">Policysettings of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5673c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5673c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5673c-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5673c-129">The resource group name.</span></span>

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

### <span data-ttu-id="5673c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5673c-130">-ResourceId</span></span>
<span data-ttu-id="5673c-131">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="5673c-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5673c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5673c-132">-Confirm</span></span>
<span data-ttu-id="5673c-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5673c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5673c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5673c-134">-WhatIf</span></span>
<span data-ttu-id="5673c-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5673c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5673c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5673c-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5673c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5673c-137">CommonParameters</span></span>
<span data-ttu-id="5673c-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5673c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5673c-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5673c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5673c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5673c-140">INPUTS</span></span>

### <span data-ttu-id="5673c-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5673c-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="5673c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5673c-142">OUTPUTS</span></span>

### <span data-ttu-id="5673c-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5673c-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="5673c-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5673c-144">NOTES</span></span>

## <span data-ttu-id="5673c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5673c-145">RELATED LINKS</span></span>
