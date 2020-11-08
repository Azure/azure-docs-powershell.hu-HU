---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194269"
---
# <span data-ttu-id="ecb01-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ecb01-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="ecb01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ecb01-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb01-103">Egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ecb01-103">Creates an application security group.</span></span>

## <span data-ttu-id="ecb01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ecb01-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecb01-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ecb01-105">DESCRIPTION</span></span>
<span data-ttu-id="ecb01-106">A **New-AzApplicationSecurityGroup** parancsmag egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ecb01-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="ecb01-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ecb01-107">EXAMPLES</span></span>

### <span data-ttu-id="ecb01-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ecb01-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="ecb01-109">Ebben a példában egy olyan alkalmazás biztonsági csoportja jön létre, amelyben nincs társítás.</span><span class="sxs-lookup"><span data-stu-id="ecb01-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="ecb01-110">Létrehozása után a hálózati felületen az IP-konfigurációk is belefoglalhatók a csoportba.</span><span class="sxs-lookup"><span data-stu-id="ecb01-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="ecb01-111">A biztonsági szabályok a csoportra a forrásként vagy a rendeltetési helyként is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="ecb01-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="ecb01-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ecb01-112">PARAMETERS</span></span>

### <span data-ttu-id="ecb01-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecb01-113">-AsJob</span></span>
<span data-ttu-id="ecb01-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ecb01-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecb01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb01-115">-DefaultProfile</span></span>
<span data-ttu-id="ecb01-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecb01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecb01-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ecb01-117">-Force</span></span>
<span data-ttu-id="ecb01-118">Ha felül szeretné írni az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecb01-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="ecb01-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="ecb01-119">-Location</span></span>
<span data-ttu-id="ecb01-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="ecb01-120">The location.</span></span>

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

### <span data-ttu-id="ecb01-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ecb01-121">-Name</span></span>
<span data-ttu-id="ecb01-122">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="ecb01-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="ecb01-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb01-123">-ResourceGroupName</span></span>
<span data-ttu-id="ecb01-124">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ecb01-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="ecb01-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="ecb01-125">-Tag</span></span>
<span data-ttu-id="ecb01-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ecb01-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ecb01-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ecb01-127">-Confirm</span></span>
<span data-ttu-id="ecb01-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecb01-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb01-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb01-129">-WhatIf</span></span>
<span data-ttu-id="ecb01-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ecb01-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb01-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecb01-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb01-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb01-132">CommonParameters</span></span>
<span data-ttu-id="ecb01-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ecb01-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb01-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb01-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb01-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecb01-135">INPUTS</span></span>

### <span data-ttu-id="ecb01-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ecb01-136">System.String</span></span>

### <span data-ttu-id="ecb01-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ecb01-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ecb01-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecb01-138">OUTPUTS</span></span>

### <span data-ttu-id="ecb01-139">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ecb01-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="ecb01-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ecb01-140">NOTES</span></span>

## <span data-ttu-id="ecb01-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecb01-141">RELATED LINKS</span></span>

[<span data-ttu-id="ecb01-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ecb01-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="ecb01-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ecb01-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="ecb01-144">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecb01-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ecb01-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecb01-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ecb01-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecb01-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ecb01-147">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecb01-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ecb01-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecb01-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ecb01-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecb01-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
