---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0bccee6b8242e3480ad405837f9c2a661eb97431
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837480"
---
# <span data-ttu-id="7a60a-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7a60a-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="7a60a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a60a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a60a-103">Egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7a60a-103">Creates an application security group.</span></span>

## <span data-ttu-id="7a60a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a60a-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a60a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a60a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a60a-106">A **New-AzApplicationSecurityGroup** parancsmag egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7a60a-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="7a60a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a60a-107">EXAMPLES</span></span>

### <span data-ttu-id="7a60a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7a60a-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="7a60a-109">Ebben a példában egy olyan alkalmazás biztonsági csoportja jön létre, amelyben nincs társítás.</span><span class="sxs-lookup"><span data-stu-id="7a60a-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="7a60a-110">Létrehozása után a hálózati felületen az IP-konfigurációk is belefoglalhatók a csoportba.</span><span class="sxs-lookup"><span data-stu-id="7a60a-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="7a60a-111">A biztonsági szabályok a csoportra a forrásként vagy a rendeltetési helyként is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="7a60a-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="7a60a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a60a-112">PARAMETERS</span></span>

### <span data-ttu-id="7a60a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a60a-113">-AsJob</span></span>
<span data-ttu-id="7a60a-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7a60a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a60a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a60a-115">-DefaultProfile</span></span>
<span data-ttu-id="7a60a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a60a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a60a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7a60a-117">-Force</span></span>
<span data-ttu-id="7a60a-118">Ha felül szeretné írni az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a60a-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="7a60a-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="7a60a-119">-Location</span></span>
<span data-ttu-id="7a60a-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="7a60a-120">The location.</span></span>

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

### <span data-ttu-id="7a60a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a60a-121">-Name</span></span>
<span data-ttu-id="7a60a-122">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="7a60a-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="7a60a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a60a-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a60a-124">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a60a-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="7a60a-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="7a60a-125">-Tag</span></span>
<span data-ttu-id="7a60a-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7a60a-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7a60a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a60a-127">-Confirm</span></span>
<span data-ttu-id="7a60a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a60a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a60a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a60a-129">-WhatIf</span></span>
<span data-ttu-id="7a60a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a60a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a60a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a60a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a60a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a60a-132">CommonParameters</span></span>
<span data-ttu-id="7a60a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a60a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a60a-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a60a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a60a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a60a-135">INPUTS</span></span>

### <span data-ttu-id="7a60a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7a60a-136">System.String</span></span>

### <span data-ttu-id="7a60a-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a60a-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7a60a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a60a-138">OUTPUTS</span></span>

### <span data-ttu-id="7a60a-139">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7a60a-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="7a60a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a60a-140">NOTES</span></span>

## <span data-ttu-id="7a60a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a60a-141">RELATED LINKS</span></span>

[<span data-ttu-id="7a60a-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7a60a-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="7a60a-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7a60a-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="7a60a-144">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a60a-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7a60a-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a60a-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7a60a-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a60a-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7a60a-147">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7a60a-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7a60a-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7a60a-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7a60a-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7a60a-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
