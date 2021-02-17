---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146954"
---
# <span data-ttu-id="48dbc-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="48dbc-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="48dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="48dbc-103">Alkalmazásbiztonsági csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="48dbc-103">Creates an application security group.</span></span>

## <span data-ttu-id="48dbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48dbc-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48dbc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48dbc-105">DESCRIPTION</span></span>
<span data-ttu-id="48dbc-106">A **New-AzApplicationSecurityGroup** parancsmag létrehoz egy alkalmazásbiztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="48dbc-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="48dbc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48dbc-107">EXAMPLES</span></span>

### <span data-ttu-id="48dbc-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="48dbc-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="48dbc-109">Ebben a példában társítások nélkül hoz létre alkalmazásbiztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="48dbc-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="48dbc-110">A létrehozása után a hálózati felületen ip-konfigurációk is szerepeltetve lesznek a csoportban.</span><span class="sxs-lookup"><span data-stu-id="48dbc-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="48dbc-111">A biztonsági szabályok a csoportra mint forrásra vagy célhelyre is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="48dbc-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="48dbc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48dbc-112">PARAMETERS</span></span>

### <span data-ttu-id="48dbc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48dbc-113">-AsJob</span></span>
<span data-ttu-id="48dbc-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="48dbc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48dbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48dbc-115">-DefaultProfile</span></span>
<span data-ttu-id="48dbc-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48dbc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48dbc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="48dbc-117">-Force</span></span>
<span data-ttu-id="48dbc-118">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="48dbc-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="48dbc-119">-Location</span><span class="sxs-lookup"><span data-stu-id="48dbc-119">-Location</span></span>
<span data-ttu-id="48dbc-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="48dbc-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48dbc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="48dbc-121">-Name</span></span>
<span data-ttu-id="48dbc-122">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="48dbc-122">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48dbc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48dbc-123">-ResourceGroupName</span></span>
<span data-ttu-id="48dbc-124">Az alkalmazás biztonsági csoportjának erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="48dbc-124">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48dbc-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="48dbc-125">-Tag</span></span>
<span data-ttu-id="48dbc-126">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="48dbc-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48dbc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48dbc-127">-Confirm</span></span>
<span data-ttu-id="48dbc-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="48dbc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48dbc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48dbc-129">-WhatIf</span></span>
<span data-ttu-id="48dbc-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="48dbc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48dbc-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48dbc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48dbc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48dbc-132">CommonParameters</span></span>
<span data-ttu-id="48dbc-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48dbc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48dbc-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48dbc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48dbc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48dbc-135">INPUTS</span></span>

### <span data-ttu-id="48dbc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="48dbc-136">System.String</span></span>

### <span data-ttu-id="48dbc-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="48dbc-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="48dbc-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48dbc-138">OUTPUTS</span></span>

### <span data-ttu-id="48dbc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="48dbc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="48dbc-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48dbc-140">NOTES</span></span>

## <span data-ttu-id="48dbc-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48dbc-141">RELATED LINKS</span></span>

[<span data-ttu-id="48dbc-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="48dbc-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="48dbc-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="48dbc-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="48dbc-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48dbc-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="48dbc-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48dbc-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="48dbc-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48dbc-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="48dbc-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="48dbc-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="48dbc-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="48dbc-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="48dbc-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="48dbc-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
