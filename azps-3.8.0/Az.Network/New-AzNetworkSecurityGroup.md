---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1ad99522e93587b2f335ae35478aedbc6cc36e88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012060"
---
# <span data-ttu-id="bba99-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bba99-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="bba99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bba99-102">SYNOPSIS</span></span>
<span data-ttu-id="bba99-103">Hálózati biztonsági csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bba99-103">Creates a network security group.</span></span>

## <span data-ttu-id="bba99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bba99-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba99-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bba99-105">DESCRIPTION</span></span>
<span data-ttu-id="bba99-106">A **New-AzNetworkSecurityGroup** parancsmag az Azure hálózat biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="bba99-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="bba99-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bba99-107">EXAMPLES</span></span>

### <span data-ttu-id="bba99-108">1: új hálózati biztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="bba99-108">1: Create a new network security group</span></span>
```
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="bba99-109">Ez a parancs létrehoz egy új Azure-hálózati biztonsági csoportot a "nsg1" nevű erőforráscsoport "rg1" nevű erőforráscsoport "westus" nevű csoportjában.</span><span class="sxs-lookup"><span data-stu-id="bba99-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="bba99-110">2: részletes hálózati biztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="bba99-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="bba99-111">Lépés: 1 biztonsági szabály létrehozása az internetről a 3389-as portra való hozzáférés engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="bba99-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="bba99-112">Lépés: 2 biztonsági szabály létrehozása, amely lehetővé teszi az internetről a 80-as port elérését.</span><span class="sxs-lookup"><span data-stu-id="bba99-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="bba99-113">Lépés: 3 vegye fel a fentiek alapján létrehozott szabályokat egy NSG-FrontEnd nevű új NSG.</span><span class="sxs-lookup"><span data-stu-id="bba99-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="bba99-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bba99-114">PARAMETERS</span></span>

### <span data-ttu-id="bba99-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bba99-115">-AsJob</span></span>
<span data-ttu-id="bba99-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bba99-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bba99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba99-117">-DefaultProfile</span></span>
<span data-ttu-id="bba99-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bba99-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bba99-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bba99-119">-Force</span></span>
<span data-ttu-id="bba99-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="bba99-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bba99-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="bba99-121">-Location</span></span>
<span data-ttu-id="bba99-122">Azt a régiót adja meg, amelyhez hálózati biztonsági csoportot szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="bba99-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="bba99-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bba99-123">-Name</span></span>
<span data-ttu-id="bba99-124">A létrehozandó hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bba99-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="bba99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba99-125">-ResourceGroupName</span></span>
<span data-ttu-id="bba99-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bba99-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bba99-127">Ez a parancsmag létrehoz egy hálózati biztonsági csoportot a paraméter által megadott erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="bba99-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bba99-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="bba99-128">-SecurityRules</span></span>
<span data-ttu-id="bba99-129">A hálózati biztonsági szabályokban létrehozott objektumok listáját adja meg, amelyek egy hálózati biztonsági csoportban hozhatók létre.</span><span class="sxs-lookup"><span data-stu-id="bba99-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba99-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="bba99-130">-Tag</span></span>
<span data-ttu-id="bba99-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="bba99-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bba99-132">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="bba99-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bba99-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bba99-133">-Confirm</span></span>
<span data-ttu-id="bba99-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bba99-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba99-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba99-135">-WhatIf</span></span>
<span data-ttu-id="bba99-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bba99-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba99-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bba99-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba99-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba99-138">CommonParameters</span></span>
<span data-ttu-id="bba99-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bba99-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba99-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba99-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba99-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bba99-141">INPUTS</span></span>

### <span data-ttu-id="bba99-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bba99-142">System.String</span></span>

### <span data-ttu-id="bba99-143">Microsoft. Azure. commands. Network. models. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="bba99-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="bba99-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bba99-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bba99-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bba99-145">OUTPUTS</span></span>

### <span data-ttu-id="bba99-146">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bba99-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="bba99-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bba99-147">NOTES</span></span>

## <span data-ttu-id="bba99-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bba99-148">RELATED LINKS</span></span>

[<span data-ttu-id="bba99-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bba99-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="bba99-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bba99-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="bba99-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bba99-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
