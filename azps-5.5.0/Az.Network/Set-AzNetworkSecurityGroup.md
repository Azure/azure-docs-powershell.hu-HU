---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158874"
---
# <span data-ttu-id="aded5-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aded5-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="aded5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aded5-102">SYNOPSIS</span></span>
<span data-ttu-id="aded5-103">Frissíti a hálózati biztonsági csoportokat.</span><span class="sxs-lookup"><span data-stu-id="aded5-103">Updates a network security group.</span></span>

## <span data-ttu-id="aded5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aded5-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aded5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aded5-105">DESCRIPTION</span></span>
<span data-ttu-id="aded5-106">A **Set-AzNetworkSecurityGroup** parancsmag frissíti a hálózati biztonsági csoportokat.</span><span class="sxs-lookup"><span data-stu-id="aded5-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="aded5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aded5-107">EXAMPLES</span></span>

### <span data-ttu-id="aded5-108">1. példa: Meglévő hálózatbiztonsági csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="aded5-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="aded5-109">Ez a parancs beolvassa az Nsg1 nevű Azure-hálózat biztonsági csoportját, és hozzáad egy Rdp-Rule nevű hálózati biztonsági szabályt, hogy az Add-AzNetworkSecurityRuleConfig használatával engedélyezze a 3389-es porton az internetes forgalmat a lekért hálózati biztonsági csoportobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="aded5-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="aded5-110">A parancs a **Set-AzNetworkSecurityGroup** használatával megmarad a módosított Azure-hálózat biztonsági csoportban.</span><span class="sxs-lookup"><span data-stu-id="aded5-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="aded5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aded5-111">PARAMETERS</span></span>

### <span data-ttu-id="aded5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aded5-112">-AsJob</span></span>
<span data-ttu-id="aded5-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aded5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aded5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aded5-114">-DefaultProfile</span></span>
<span data-ttu-id="aded5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aded5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aded5-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aded5-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="aded5-117">Egy hálózati biztonsági csoportobjektumot ad meg, amely azt az állapotot képviseli, amelyben a hálózatbiztonsági csoportot be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="aded5-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="aded5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aded5-118">-Confirm</span></span>
<span data-ttu-id="aded5-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aded5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aded5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aded5-120">-WhatIf</span></span>
<span data-ttu-id="aded5-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aded5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aded5-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aded5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aded5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aded5-123">CommonParameters</span></span>
<span data-ttu-id="aded5-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aded5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aded5-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aded5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aded5-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aded5-126">INPUTS</span></span>

### <span data-ttu-id="aded5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aded5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="aded5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aded5-128">OUTPUTS</span></span>

### <span data-ttu-id="aded5-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aded5-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="aded5-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aded5-130">NOTES</span></span>

## <span data-ttu-id="aded5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aded5-131">RELATED LINKS</span></span>

[<span data-ttu-id="aded5-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aded5-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="aded5-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aded5-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="aded5-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aded5-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


