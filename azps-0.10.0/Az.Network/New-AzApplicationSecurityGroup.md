---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 81eaa1f5c6e44586ae6ac9e5b6838f00063a9211
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841370"
---
# <span data-ttu-id="4e13d-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e13d-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="4e13d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e13d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e13d-103">Egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4e13d-103">Creates an application security group.</span></span>

## <span data-ttu-id="4e13d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e13d-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e13d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e13d-105">DESCRIPTION</span></span>
<span data-ttu-id="4e13d-106">A **New-AzApplicationSecurityGroup** parancsmag egy alkalmazás biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4e13d-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="4e13d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4e13d-107">EXAMPLES</span></span>

### <span data-ttu-id="4e13d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4e13d-108">Example 1</span></span>
```
PS C:\> New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="4e13d-109">Ebben a példában egy olyan alkalmazás biztonsági csoportja jön létre, amelyben nincs társítás.</span><span class="sxs-lookup"><span data-stu-id="4e13d-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="4e13d-110">Létrehozása után a hálózati felületen az IP-konfigurációk is belefoglalhatók a csoportba.</span><span class="sxs-lookup"><span data-stu-id="4e13d-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="4e13d-111">A biztonsági szabályok a csoportra a forrásként vagy a rendeltetési helyként is hivatkozhatnak.</span><span class="sxs-lookup"><span data-stu-id="4e13d-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="4e13d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e13d-112">PARAMETERS</span></span>

### <span data-ttu-id="4e13d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e13d-113">-AsJob</span></span>
<span data-ttu-id="4e13d-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4e13d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e13d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e13d-115">-DefaultProfile</span></span>
<span data-ttu-id="4e13d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e13d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e13d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4e13d-117">-Force</span></span>
<span data-ttu-id="4e13d-118">Ha felül szeretné írni az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e13d-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="4e13d-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="4e13d-119">-Location</span></span>
<span data-ttu-id="4e13d-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="4e13d-120">The location.</span></span>

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

### <span data-ttu-id="4e13d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e13d-121">-Name</span></span>
<span data-ttu-id="4e13d-122">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="4e13d-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="4e13d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e13d-123">-ResourceGroupName</span></span>
<span data-ttu-id="4e13d-124">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e13d-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="4e13d-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="4e13d-125">-Tag</span></span>
<span data-ttu-id="4e13d-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4e13d-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4e13d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e13d-127">-Confirm</span></span>
<span data-ttu-id="4e13d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e13d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e13d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e13d-129">-WhatIf</span></span>
<span data-ttu-id="4e13d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e13d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e13d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e13d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e13d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e13d-132">CommonParameters</span></span>
<span data-ttu-id="4e13d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e13d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e13d-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e13d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e13d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e13d-135">INPUTS</span></span>

### <span data-ttu-id="4e13d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4e13d-136">System.String</span></span>
<span data-ttu-id="4e13d-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e13d-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4e13d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e13d-138">OUTPUTS</span></span>

### <span data-ttu-id="4e13d-139">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e13d-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="4e13d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e13d-140">NOTES</span></span>

## <span data-ttu-id="4e13d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e13d-141">RELATED LINKS</span></span>

[<span data-ttu-id="4e13d-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e13d-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4e13d-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e13d-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4e13d-144">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e13d-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4e13d-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e13d-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4e13d-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e13d-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4e13d-147">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4e13d-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4e13d-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4e13d-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4e13d-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4e13d-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
