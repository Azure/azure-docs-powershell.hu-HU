---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 78380af20ce5905b5c004424c1e17ac977de40ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669987"
---
# <span data-ttu-id="1c6a3-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a3-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="1c6a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6a3-103">Egy hálózati biztonsági csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="1c6a3-103">Updates a network security group.</span></span>

## <span data-ttu-id="1c6a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c6a3-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c6a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c6a3-105">DESCRIPTION</span></span>
<span data-ttu-id="1c6a3-106">A **set-AzNetworkSecurityGroup** parancsmag frissíti a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="1c6a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1c6a3-107">EXAMPLES</span></span>

### <span data-ttu-id="1c6a3-108">Példa 1: meglévő hálózati biztonsági csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="1c6a3-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="1c6a3-109">Ez a parancs beolvassa a Nsg1 nevű Azure hálózat biztonsági csoportját, és felvesz egy Rdp-Rule nevű hálózati biztonsági szabályt, amely lehetővé teszi a 3389-as porton lévő internetes forgalom engedélyezését a AzNetworkSecurityRuleConfig segítségével.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="1c6a3-110">A parancs a **set-AzNetworkSecurityGroup** használatával megmarad a módosított Azure hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="1c6a3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c6a3-111">PARAMETERS</span></span>

### <span data-ttu-id="1c6a3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c6a3-112">-AsJob</span></span>
<span data-ttu-id="1c6a3-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1c6a3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c6a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6a3-114">-DefaultProfile</span></span>
<span data-ttu-id="1c6a3-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c6a3-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a3-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1c6a3-117">Itt adhatja meg azt az állapotot megjelenítő hálózatbiztonsági Csoport objektumát, amelybe a hálózat biztonsági csoportját be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="1c6a3-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1c6a3-118">-Confirm</span></span>
<span data-ttu-id="1c6a3-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6a3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6a3-120">-WhatIf</span></span>
<span data-ttu-id="1c6a3-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c6a3-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6a3-123">CommonParameters</span></span>
<span data-ttu-id="1c6a3-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c6a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6a3-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6a3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6a3-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c6a3-126">INPUTS</span></span>

### <span data-ttu-id="1c6a3-127">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a3-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1c6a3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c6a3-128">OUTPUTS</span></span>

### <span data-ttu-id="1c6a3-129">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a3-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1c6a3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c6a3-130">NOTES</span></span>

## <span data-ttu-id="1c6a3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c6a3-131">RELATED LINKS</span></span>

[<span data-ttu-id="1c6a3-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a3-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="1c6a3-133">Új – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a3-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="1c6a3-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a3-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


