---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188246"
---
# <span data-ttu-id="806e3-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="806e3-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="806e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="806e3-102">SYNOPSIS</span></span>
<span data-ttu-id="806e3-103">Az alkalmazás-átjáró tűzfal-házirendjének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="806e3-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="806e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="806e3-104">SYNTAX</span></span>

### <span data-ttu-id="806e3-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="806e3-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="806e3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="806e3-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="806e3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="806e3-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="806e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="806e3-108">DESCRIPTION</span></span>
<span data-ttu-id="806e3-109">A **Remove-AzApplicationGatewayFirewallPolicy** parancsmag eltávolítja az alkalmazás-átjáró tűzfal-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="806e3-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="806e3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="806e3-110">EXAMPLES</span></span>

### <span data-ttu-id="806e3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="806e3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="806e3-112">Ez a parancs eltávolítja a ApplicationGatewayFirewallPolicy01 nevű alkalmazás-átjáró nevű tűzfal-házirendet az ResourceGroup01 nevű erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="806e3-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="806e3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="806e3-113">PARAMETERS</span></span>

### <span data-ttu-id="806e3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="806e3-114">-AsJob</span></span>
<span data-ttu-id="806e3-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="806e3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="806e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806e3-116">-DefaultProfile</span></span>
<span data-ttu-id="806e3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="806e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="806e3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="806e3-118">-Force</span></span>
<span data-ttu-id="806e3-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="806e3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="806e3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="806e3-120">-InputObject</span></span>
<span data-ttu-id="806e3-121">A tűzfal házirend-objektuma</span><span class="sxs-lookup"><span data-stu-id="806e3-121">The firewall policy object</span></span>

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

### <span data-ttu-id="806e3-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="806e3-122">-Name</span></span>
<span data-ttu-id="806e3-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="806e3-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806e3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="806e3-124">-PassThru</span></span>
<span data-ttu-id="806e3-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="806e3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="806e3-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="806e3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="806e3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806e3-127">-ResourceGroupName</span></span>
<span data-ttu-id="806e3-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="806e3-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806e3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="806e3-129">-ResourceId</span></span>
<span data-ttu-id="806e3-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="806e3-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="806e3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="806e3-131">-Confirm</span></span>
<span data-ttu-id="806e3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="806e3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="806e3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="806e3-133">-WhatIf</span></span>
<span data-ttu-id="806e3-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="806e3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="806e3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="806e3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="806e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806e3-136">CommonParameters</span></span>
<span data-ttu-id="806e3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="806e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806e3-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="806e3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806e3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="806e3-139">INPUTS</span></span>

### <span data-ttu-id="806e3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="806e3-140">System.String</span></span>

## <span data-ttu-id="806e3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="806e3-141">OUTPUTS</span></span>

### <span data-ttu-id="806e3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="806e3-142">System.Boolean</span></span>

## <span data-ttu-id="806e3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="806e3-143">NOTES</span></span>

## <span data-ttu-id="806e3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="806e3-144">RELATED LINKS</span></span>
