---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a60fa0e305d05ae5d944a69705c3cb3f392b28f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940082"
---
# <span data-ttu-id="41430-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41430-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="41430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41430-102">SYNOPSIS</span></span>
<span data-ttu-id="41430-103">Eltávolít egy hálózati biztonsági szabályt egy hálózati biztonsági csoportból.</span><span class="sxs-lookup"><span data-stu-id="41430-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="41430-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41430-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41430-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41430-105">DESCRIPTION</span></span>
<span data-ttu-id="41430-106">A **Remove-AzNetworkSecurityRuleConfig** parancsmag eltávolítja egy hálózati biztonsági szabály konfigurációját egy Azure-hálózati biztonsági csoportból.</span><span class="sxs-lookup"><span data-stu-id="41430-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="41430-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41430-107">EXAMPLES</span></span>

### <span data-ttu-id="41430-108">1. példa: Hálózati biztonsági szabály konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="41430-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="41430-109">Az első parancs létrehoz egy rdp-rule nevű hálózati biztonsági szabály-konfigurációt, majd azt a $rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="41430-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="41430-110">A második parancs létrehoz egy hálózati biztonsági csoportot a $rule 1 szabály használatával, majd a hálózati biztonsági csoportot a $nsg változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="41430-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="41430-111">A harmadik parancs eltávolítja az RDP-szabály nevű hálózati biztonsági szabály konfigurációját a helyi $nsg.</span><span class="sxs-lookup"><span data-stu-id="41430-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="41430-112">A oda-vissza parancs menti a változást.</span><span class="sxs-lookup"><span data-stu-id="41430-112">The forth command saves the change.</span></span>

## <span data-ttu-id="41430-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41430-113">PARAMETERS</span></span>

### <span data-ttu-id="41430-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41430-114">-DefaultProfile</span></span>
<span data-ttu-id="41430-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41430-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41430-116">-Name</span><span class="sxs-lookup"><span data-stu-id="41430-116">-Name</span></span>
<span data-ttu-id="41430-117">Annak a hálózati biztonsági szabálynak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="41430-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="41430-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41430-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="41430-119">**NetworkSecurityGroup-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="41430-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="41430-120">Ez az objektum az eltávolítható hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="41430-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="41430-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41430-121">CommonParameters</span></span>
<span data-ttu-id="41430-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41430-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41430-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41430-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41430-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41430-124">INPUTS</span></span>

### <span data-ttu-id="41430-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41430-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="41430-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41430-126">OUTPUTS</span></span>

### <span data-ttu-id="41430-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41430-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="41430-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41430-128">NOTES</span></span>

## <span data-ttu-id="41430-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41430-129">RELATED LINKS</span></span>

[<span data-ttu-id="41430-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41430-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41430-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41430-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41430-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41430-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="41430-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41430-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41430-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41430-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


