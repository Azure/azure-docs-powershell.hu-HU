---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: d6ca2ac1e091e3576af51ba8f1a2f50676994ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503527"
---
# <span data-ttu-id="7631d-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7631d-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7631d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7631d-102">SYNOPSIS</span></span>
<span data-ttu-id="7631d-103">Hálózati biztonsági szabály eltávolítása hálózati biztonsági csoportból</span><span class="sxs-lookup"><span data-stu-id="7631d-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7631d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7631d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7631d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7631d-105">DESCRIPTION</span></span>
<span data-ttu-id="7631d-106">A **Remove-AzureRmNetworkSecurityRuleConfig** parancsmag a hálózat biztonsági szabályait az Azure hálózat biztonsági csoportjaiból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="7631d-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="7631d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7631d-107">EXAMPLES</span></span>

### <span data-ttu-id="7631d-108">1. példa: hálózatbiztonsági szabály konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7631d-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="7631d-109">Az első parancs létrehoz egy RDP-Rule nevű hálózati biztonsági szabály konfigurációját, és a $rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7631d-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="7631d-110">A második parancs a $rule 1 szabály segítségével hoz létre hálózati biztonsági csoportot, majd a $nsg változóban tárolja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="7631d-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="7631d-111">A harmadik parancs eltávolítja az RDP-Rule nevű hálózati biztonsági szabály konfigurációját a $nsg hálózati biztonsági csoportból.</span><span class="sxs-lookup"><span data-stu-id="7631d-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="7631d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7631d-112">PARAMETERS</span></span>

### <span data-ttu-id="7631d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7631d-113">-DefaultProfile</span></span>
<span data-ttu-id="7631d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7631d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7631d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7631d-115">-Name</span></span>
<span data-ttu-id="7631d-116">A parancsmag által eltávolított hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7631d-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7631d-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7631d-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7631d-118">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7631d-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="7631d-119">Ez az objektum az eltávolítandó hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7631d-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="7631d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7631d-120">CommonParameters</span></span>
<span data-ttu-id="7631d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7631d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7631d-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7631d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7631d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7631d-123">INPUTS</span></span>

### <span data-ttu-id="7631d-124">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7631d-124">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="7631d-125">Paraméterek: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7631d-125">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="7631d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7631d-126">OUTPUTS</span></span>

### <span data-ttu-id="7631d-127">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7631d-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7631d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7631d-128">NOTES</span></span>

## <span data-ttu-id="7631d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7631d-129">RELATED LINKS</span></span>

[<span data-ttu-id="7631d-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7631d-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7631d-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7631d-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7631d-132">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7631d-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="7631d-133">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7631d-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7631d-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7631d-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

