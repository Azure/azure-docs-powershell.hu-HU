---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 1252c452cc6ad7996a8dcddcb915da251b0b5039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670139"
---
# <span data-ttu-id="64032-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64032-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="64032-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64032-102">SYNOPSIS</span></span>
<span data-ttu-id="64032-103">Hálózati biztonsági szabály eltávolítása hálózati biztonsági csoportból</span><span class="sxs-lookup"><span data-stu-id="64032-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="64032-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64032-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64032-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64032-105">DESCRIPTION</span></span>
<span data-ttu-id="64032-106">A **Remove-AzNetworkSecurityRuleConfig** parancsmag a hálózat biztonsági szabályait az Azure hálózat biztonsági csoportjaiból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="64032-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="64032-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64032-107">EXAMPLES</span></span>

### <span data-ttu-id="64032-108">1. példa: hálózatbiztonsági szabály konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="64032-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="64032-109">Az első parancs létrehoz egy RDP-Rule nevű hálózati biztonsági szabály konfigurációját, és a $rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="64032-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="64032-110">A második parancs a $rule 1 szabály segítségével hoz létre hálózati biztonsági csoportot, majd a $nsg változóban tárolja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="64032-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="64032-111">A harmadik parancs eltávolítja az RDP-Rule nevű hálózati biztonsági szabály konfigurációját a $nsg hálózati biztonsági csoportból.</span><span class="sxs-lookup"><span data-stu-id="64032-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="64032-112">A Forth parancs menti a változást.</span><span class="sxs-lookup"><span data-stu-id="64032-112">The forth command saves the change.</span></span>

## <span data-ttu-id="64032-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64032-113">PARAMETERS</span></span>

### <span data-ttu-id="64032-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64032-114">-DefaultProfile</span></span>
<span data-ttu-id="64032-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64032-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64032-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64032-116">-Name</span></span>
<span data-ttu-id="64032-117">A parancsmag által eltávolított hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64032-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64032-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64032-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="64032-119">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="64032-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="64032-120">Ez az objektum az eltávolítandó hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64032-120">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64032-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64032-121">CommonParameters</span></span>
<span data-ttu-id="64032-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64032-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64032-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64032-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64032-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64032-124">INPUTS</span></span>

### <span data-ttu-id="64032-125">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64032-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="64032-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64032-126">OUTPUTS</span></span>

### <span data-ttu-id="64032-127">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64032-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="64032-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64032-128">NOTES</span></span>

## <span data-ttu-id="64032-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64032-129">RELATED LINKS</span></span>

[<span data-ttu-id="64032-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64032-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="64032-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64032-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="64032-132">Új – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64032-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="64032-133">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64032-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="64032-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64032-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


