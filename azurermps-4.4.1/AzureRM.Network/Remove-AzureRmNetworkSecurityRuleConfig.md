---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 1f221e16d75ac776538319ff82c1b7dc1a3d200b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492459"
---
# <span data-ttu-id="6a597-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6a597-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="6a597-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a597-102">SYNOPSIS</span></span>
<span data-ttu-id="6a597-103">Hálózati biztonsági szabály eltávolítása hálózati biztonsági csoportból</span><span class="sxs-lookup"><span data-stu-id="6a597-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a597-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a597-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a597-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a597-105">DESCRIPTION</span></span>
<span data-ttu-id="6a597-106">A **Remove-AzureRmNetworkSecurityRuleConfig** parancsmag a hálózat biztonsági szabályait az Azure hálózat biztonsági csoportjaiból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="6a597-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="6a597-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a597-107">EXAMPLES</span></span>

### <span data-ttu-id="6a597-108">1. példa: hálózatbiztonsági szabály konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6a597-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="6a597-109">Az első parancs létrehoz egy RDP-Rule nevű hálózati biztonsági szabály konfigurációját, és a $rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6a597-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="6a597-110">A második parancs a $rule 1 szabály segítségével hoz létre hálózati biztonsági csoportot, majd a $nsg változóban tárolja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="6a597-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="6a597-111">A harmadik parancs eltávolítja az RDP-Rule nevű hálózati biztonsági szabály konfigurációját a $nsg hálózati biztonsági csoportból.</span><span class="sxs-lookup"><span data-stu-id="6a597-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="6a597-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a597-112">PARAMETERS</span></span>

### <span data-ttu-id="6a597-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a597-113">-DefaultProfile</span></span>
<span data-ttu-id="6a597-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a597-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a597-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a597-115">-Name</span></span>
<span data-ttu-id="6a597-116">A parancsmag által eltávolított hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a597-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a597-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6a597-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="6a597-118">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6a597-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="6a597-119">Ez az objektum az eltávolítandó hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a597-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="6a597-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a597-120">CommonParameters</span></span>
<span data-ttu-id="6a597-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a597-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a597-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a597-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a597-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a597-123">INPUTS</span></span>

### <span data-ttu-id="6a597-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6a597-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="6a597-125">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6a597-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="6a597-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a597-126">OUTPUTS</span></span>

### <span data-ttu-id="6a597-127">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6a597-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="6a597-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a597-128">NOTES</span></span>

## <span data-ttu-id="6a597-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a597-129">RELATED LINKS</span></span>

[<span data-ttu-id="6a597-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6a597-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6a597-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6a597-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6a597-132">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6a597-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="6a597-133">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6a597-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6a597-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6a597-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


