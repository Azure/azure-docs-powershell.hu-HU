---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202653"
---
# <span data-ttu-id="491fe-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="491fe-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="491fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="491fe-102">SYNOPSIS</span></span>
<span data-ttu-id="491fe-103">Eltávolít egy alkalmazás átjáró tűzfal házirendet.</span><span class="sxs-lookup"><span data-stu-id="491fe-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="491fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="491fe-104">SYNTAX</span></span>

### <span data-ttu-id="491fe-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="491fe-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="491fe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="491fe-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="491fe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="491fe-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491fe-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="491fe-108">DESCRIPTION</span></span>
<span data-ttu-id="491fe-109">A **Remove-AzApplicationGatewayFirewallPolicy** parancsmag eltávolít egy alkalmazás-átjáró tűzfalházira vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="491fe-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="491fe-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="491fe-110">EXAMPLES</span></span>

### <span data-ttu-id="491fe-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="491fe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="491fe-112">Ez a parancs eltávolítja az ApplicationGatewayFirewallPolicy01 nevű alkalmazás-átjáró tűzfal házirendet az ResourceGroup01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="491fe-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="491fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="491fe-113">PARAMETERS</span></span>

### <span data-ttu-id="491fe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="491fe-114">-AsJob</span></span>
<span data-ttu-id="491fe-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="491fe-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="491fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491fe-116">-DefaultProfile</span></span>
<span data-ttu-id="491fe-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="491fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="491fe-118">-Force</span><span class="sxs-lookup"><span data-stu-id="491fe-118">-Force</span></span>
<span data-ttu-id="491fe-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="491fe-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="491fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="491fe-120">-InputObject</span></span>
<span data-ttu-id="491fe-121">A tűzfal házirendobjektuma</span><span class="sxs-lookup"><span data-stu-id="491fe-121">The firewall policy object</span></span>

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

### <span data-ttu-id="491fe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="491fe-122">-Name</span></span>
<span data-ttu-id="491fe-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="491fe-123">The resource name.</span></span>

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

### <span data-ttu-id="491fe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="491fe-124">-PassThru</span></span>
<span data-ttu-id="491fe-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="491fe-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="491fe-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="491fe-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="491fe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="491fe-127">-ResourceGroupName</span></span>
<span data-ttu-id="491fe-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="491fe-128">The resource group name.</span></span>

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

### <span data-ttu-id="491fe-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="491fe-129">-ResourceId</span></span>
<span data-ttu-id="491fe-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="491fe-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="491fe-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="491fe-131">-Confirm</span></span>
<span data-ttu-id="491fe-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="491fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="491fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491fe-133">-WhatIf</span></span>
<span data-ttu-id="491fe-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="491fe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="491fe-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="491fe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="491fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491fe-136">CommonParameters</span></span>
<span data-ttu-id="491fe-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="491fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491fe-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="491fe-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491fe-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="491fe-139">INPUTS</span></span>

### <span data-ttu-id="491fe-140">System.String</span><span class="sxs-lookup"><span data-stu-id="491fe-140">System.String</span></span>

## <span data-ttu-id="491fe-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="491fe-141">OUTPUTS</span></span>

### <span data-ttu-id="491fe-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="491fe-142">System.Boolean</span></span>

## <span data-ttu-id="491fe-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="491fe-143">NOTES</span></span>

## <span data-ttu-id="491fe-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="491fe-144">RELATED LINKS</span></span>
