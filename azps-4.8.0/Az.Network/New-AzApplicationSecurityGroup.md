---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181581"
---
# <span data-ttu-id="e6692-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e6692-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="e6692-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6692-102">SYNOPSIS</span></span>
<span data-ttu-id="e6692-103">Egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e6692-103">Creates an application security group.</span></span>

## <span data-ttu-id="e6692-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6692-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6692-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6692-105">DESCRIPTION</span></span>
<span data-ttu-id="e6692-106">A **New-AzApplicationSecurityGroup** parancsmag egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e6692-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="e6692-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6692-107">EXAMPLES</span></span>

### <span data-ttu-id="e6692-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6692-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="e6692-109">Ebben a példában egy olyan alkalmazás biztonsági csoportja jön létre, amelyben nincs társítás.</span><span class="sxs-lookup"><span data-stu-id="e6692-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="e6692-110">Létrehozása után a hálózati felületen az IP-konfigurációk is belefoglalhatók a csoportba.</span><span class="sxs-lookup"><span data-stu-id="e6692-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="e6692-111">A biztonsági szabályok a csoportra a forrásként vagy a rendeltetési helyként is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="e6692-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="e6692-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6692-112">PARAMETERS</span></span>

### <span data-ttu-id="e6692-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6692-113">-AsJob</span></span>
<span data-ttu-id="e6692-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6692-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6692-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6692-115">-DefaultProfile</span></span>
<span data-ttu-id="e6692-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6692-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6692-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e6692-117">-Force</span></span>
<span data-ttu-id="e6692-118">Ha felül szeretné írni az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6692-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="e6692-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="e6692-119">-Location</span></span>
<span data-ttu-id="e6692-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="e6692-120">The location.</span></span>

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

### <span data-ttu-id="e6692-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6692-121">-Name</span></span>
<span data-ttu-id="e6692-122">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="e6692-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="e6692-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6692-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6692-124">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6692-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="e6692-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="e6692-125">-Tag</span></span>
<span data-ttu-id="e6692-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e6692-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e6692-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6692-127">-Confirm</span></span>
<span data-ttu-id="e6692-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6692-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6692-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6692-129">-WhatIf</span></span>
<span data-ttu-id="e6692-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6692-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6692-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6692-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6692-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6692-132">CommonParameters</span></span>
<span data-ttu-id="e6692-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6692-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6692-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6692-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6692-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6692-135">INPUTS</span></span>

### <span data-ttu-id="e6692-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e6692-136">System.String</span></span>

### <span data-ttu-id="e6692-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6692-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e6692-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6692-138">OUTPUTS</span></span>

### <span data-ttu-id="e6692-139">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e6692-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="e6692-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6692-140">NOTES</span></span>

## <span data-ttu-id="e6692-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6692-141">RELATED LINKS</span></span>

[<span data-ttu-id="e6692-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e6692-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="e6692-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e6692-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="e6692-144">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6692-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e6692-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6692-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e6692-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6692-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e6692-147">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6692-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e6692-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6692-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e6692-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6692-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
