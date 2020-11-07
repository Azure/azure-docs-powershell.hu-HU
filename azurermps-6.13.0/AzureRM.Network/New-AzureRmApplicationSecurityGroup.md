---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 359b98d19edfdbdd3c1ce8d6ab7286f13cf5dbfa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680642"
---
# <span data-ttu-id="19449-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19449-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="19449-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19449-102">SYNOPSIS</span></span>
<span data-ttu-id="19449-103">Egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="19449-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19449-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19449-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19449-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19449-105">DESCRIPTION</span></span>
<span data-ttu-id="19449-106">A **New-AzureRmApplicationSecurityGroup** parancsmag egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="19449-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="19449-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19449-107">EXAMPLES</span></span>

### <span data-ttu-id="19449-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19449-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="19449-109">Ebben a példában egy olyan alkalmazás biztonsági csoportja jön létre, amelyben nincs társítás.</span><span class="sxs-lookup"><span data-stu-id="19449-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="19449-110">Létrehozása után a hálózati felületen az IP-konfigurációk is belefoglalhatók a csoportba.</span><span class="sxs-lookup"><span data-stu-id="19449-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="19449-111">A biztonsági szabályok a csoportra a forrásként vagy a rendeltetési helyként is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="19449-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="19449-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19449-112">PARAMETERS</span></span>

### <span data-ttu-id="19449-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19449-113">-AsJob</span></span>
<span data-ttu-id="19449-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="19449-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19449-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19449-115">-DefaultProfile</span></span>
<span data-ttu-id="19449-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19449-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19449-117">-Force</span><span class="sxs-lookup"><span data-stu-id="19449-117">-Force</span></span>
<span data-ttu-id="19449-118">Ha felül szeretné írni az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19449-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="19449-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="19449-119">-Location</span></span>
<span data-ttu-id="19449-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="19449-120">The location.</span></span>

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

### <span data-ttu-id="19449-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19449-121">-Name</span></span>
<span data-ttu-id="19449-122">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="19449-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="19449-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19449-123">-ResourceGroupName</span></span>
<span data-ttu-id="19449-124">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="19449-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="19449-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="19449-125">-Tag</span></span>
<span data-ttu-id="19449-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="19449-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="19449-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19449-127">-Confirm</span></span>
<span data-ttu-id="19449-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19449-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19449-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19449-129">-WhatIf</span></span>
<span data-ttu-id="19449-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19449-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19449-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19449-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19449-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19449-132">CommonParameters</span></span>
<span data-ttu-id="19449-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19449-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19449-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19449-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19449-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19449-135">INPUTS</span></span>

### <span data-ttu-id="19449-136">System. String</span><span class="sxs-lookup"><span data-stu-id="19449-136">System.String</span></span>

### <span data-ttu-id="19449-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19449-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="19449-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19449-138">OUTPUTS</span></span>

### <span data-ttu-id="19449-139">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19449-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="19449-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19449-140">NOTES</span></span>

## <span data-ttu-id="19449-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19449-141">RELATED LINKS</span></span>

[<span data-ttu-id="19449-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19449-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="19449-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19449-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="19449-144">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19449-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="19449-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19449-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="19449-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19449-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="19449-147">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19449-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="19449-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19449-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="19449-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19449-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
