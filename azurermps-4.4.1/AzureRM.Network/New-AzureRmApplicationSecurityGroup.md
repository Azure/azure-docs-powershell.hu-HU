---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679754"
---
# <span data-ttu-id="f39aa-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f39aa-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="f39aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f39aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f39aa-103">Egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f39aa-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f39aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f39aa-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f39aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f39aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f39aa-106">A **New-AzureRmApplicationSecurityGroup** parancsmag egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f39aa-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="f39aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f39aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f39aa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f39aa-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="f39aa-109">Ebben a példában egy olyan alkalmazás biztonsági csoportja jön létre, amelyben nincs társítás.</span><span class="sxs-lookup"><span data-stu-id="f39aa-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="f39aa-110">Létrehozása után a hálózati felületen az IP-konfigurációk is belefoglalhatók a csoportba.</span><span class="sxs-lookup"><span data-stu-id="f39aa-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="f39aa-111">A biztonsági szabályok a csoportra a forrásként vagy a rendeltetési helyként is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="f39aa-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="f39aa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f39aa-112">PARAMETERS</span></span>

### <span data-ttu-id="f39aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39aa-113">-DefaultProfile</span></span>
<span data-ttu-id="f39aa-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f39aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f39aa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f39aa-115">-Force</span></span>
<span data-ttu-id="f39aa-116">Ha felül szeretné írni az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f39aa-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="f39aa-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="f39aa-117">-Location</span></span>
<span data-ttu-id="f39aa-118">A hely.</span><span class="sxs-lookup"><span data-stu-id="f39aa-118">The location.</span></span>

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

### <span data-ttu-id="f39aa-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f39aa-119">-Name</span></span>
<span data-ttu-id="f39aa-120">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="f39aa-120">The name of the application security group.</span></span>

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

### <span data-ttu-id="f39aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="f39aa-122">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f39aa-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="f39aa-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="f39aa-123">-Tag</span></span>
<span data-ttu-id="f39aa-124">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f39aa-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f39aa-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f39aa-125">-Confirm</span></span>
<span data-ttu-id="f39aa-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f39aa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39aa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39aa-127">-WhatIf</span></span>
<span data-ttu-id="f39aa-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f39aa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f39aa-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f39aa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39aa-130">CommonParameters</span></span>
<span data-ttu-id="f39aa-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f39aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39aa-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39aa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39aa-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f39aa-133">INPUTS</span></span>

### <span data-ttu-id="f39aa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f39aa-134">System.String</span></span>
<span data-ttu-id="f39aa-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f39aa-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f39aa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f39aa-136">OUTPUTS</span></span>

### <span data-ttu-id="f39aa-137">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f39aa-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="f39aa-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f39aa-138">NOTES</span></span>

## <span data-ttu-id="f39aa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f39aa-139">RELATED LINKS</span></span>

[<span data-ttu-id="f39aa-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f39aa-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="f39aa-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f39aa-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="f39aa-142">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f39aa-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f39aa-143">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f39aa-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f39aa-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f39aa-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f39aa-145">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f39aa-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f39aa-146">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f39aa-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f39aa-147">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f39aa-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
