---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 99c863861bdf6a434e1268dcb1d9dd55ff8d9f80
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848417"
---
# <span data-ttu-id="e3e89-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3e89-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="e3e89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3e89-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e89-103">Egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e3e89-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3e89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3e89-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3e89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3e89-105">DESCRIPTION</span></span>
<span data-ttu-id="e3e89-106">A **New-AzureRmApplicationSecurityGroup** parancsmag egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e3e89-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="e3e89-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3e89-107">EXAMPLES</span></span>

### <span data-ttu-id="e3e89-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3e89-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="e3e89-109">Ebben a példában egy olyan alkalmazás biztonsági csoportja jön létre, amelyben nincs társítás.</span><span class="sxs-lookup"><span data-stu-id="e3e89-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="e3e89-110">Létrehozása után a hálózati felületen az IP-konfigurációk is belefoglalhatók a csoportba.</span><span class="sxs-lookup"><span data-stu-id="e3e89-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="e3e89-111">A biztonsági szabályok a csoportra a forrásként vagy a rendeltetési helyként is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="e3e89-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="e3e89-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3e89-112">PARAMETERS</span></span>

### <span data-ttu-id="e3e89-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3e89-113">-AsJob</span></span>
<span data-ttu-id="e3e89-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e3e89-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e89-115">-DefaultProfile</span></span>
<span data-ttu-id="e3e89-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3e89-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e3e89-117">-Force</span></span>
<span data-ttu-id="e3e89-118">Ha felül szeretné írni az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3e89-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="e3e89-119">-Location</span></span>
<span data-ttu-id="e3e89-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="e3e89-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3e89-121">-Name</span></span>
<span data-ttu-id="e3e89-122">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="e3e89-122">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e89-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3e89-124">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3e89-124">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="e3e89-125">-Tag</span></span>
<span data-ttu-id="e3e89-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e3e89-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3e89-127">-Confirm</span></span>
<span data-ttu-id="e3e89-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3e89-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e89-129">-WhatIf</span></span>
<span data-ttu-id="e3e89-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3e89-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e89-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3e89-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e89-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e89-132">CommonParameters</span></span>
<span data-ttu-id="e3e89-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3e89-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e89-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e89-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e89-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3e89-135">INPUTS</span></span>

### <span data-ttu-id="e3e89-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e3e89-136">System.String</span></span>
<span data-ttu-id="e3e89-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3e89-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3e89-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3e89-138">OUTPUTS</span></span>

### <span data-ttu-id="e3e89-139">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3e89-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="e3e89-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3e89-140">NOTES</span></span>

## <span data-ttu-id="e3e89-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3e89-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3e89-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3e89-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="e3e89-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3e89-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="e3e89-144">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3e89-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e3e89-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3e89-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e3e89-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3e89-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e3e89-147">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3e89-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e3e89-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3e89-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e3e89-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3e89-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
