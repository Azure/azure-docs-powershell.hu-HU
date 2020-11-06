---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: d2ec8299ff2554621fc8d0952308300b6a225205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500499"
---
# <span data-ttu-id="efa61-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa61-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="efa61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efa61-102">SYNOPSIS</span></span>
<span data-ttu-id="efa61-103">Hálózati biztonsági csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="efa61-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efa61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efa61-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efa61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="efa61-105">DESCRIPTION</span></span>
<span data-ttu-id="efa61-106">A **New-AzureRmNetworkSecurityGroup** parancsmag az Azure hálózat biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="efa61-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="efa61-107">Példák</span><span class="sxs-lookup"><span data-stu-id="efa61-107">EXAMPLES</span></span>

### <span data-ttu-id="efa61-108">1: új hálózati biztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="efa61-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="efa61-109">Ez a parancs létrehoz egy új Azure-hálózati biztonsági csoportot a "nsg1" nevű erőforráscsoport "rg1" nevű erőforráscsoport "westus" nevű csoportjában.</span><span class="sxs-lookup"><span data-stu-id="efa61-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="efa61-110">2: részletes hálózati biztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="efa61-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="efa61-111">Lépés: 1 biztonsági szabály létrehozása az internetről a 3389-as portra való hozzáférés engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="efa61-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="efa61-112">Lépés: 2 biztonsági szabály létrehozása, amely lehetővé teszi az internetről a 80-as port elérését.</span><span class="sxs-lookup"><span data-stu-id="efa61-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="efa61-113">Lépés: 3 vegye fel a fentiek alapján létrehozott szabályokat egy NSG-FrontEnd nevű új NSG.</span><span class="sxs-lookup"><span data-stu-id="efa61-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="efa61-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efa61-114">PARAMETERS</span></span>

### <span data-ttu-id="efa61-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efa61-115">-AsJob</span></span>
<span data-ttu-id="efa61-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="efa61-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efa61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa61-117">-DefaultProfile</span></span>
<span data-ttu-id="efa61-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efa61-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa61-119">-Force</span><span class="sxs-lookup"><span data-stu-id="efa61-119">-Force</span></span>
<span data-ttu-id="efa61-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="efa61-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="efa61-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="efa61-121">-Location</span></span>
<span data-ttu-id="efa61-122">Azt a régiót adja meg, amelyhez hálózati biztonsági csoportot szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="efa61-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="efa61-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="efa61-123">-Name</span></span>
<span data-ttu-id="efa61-124">A létrehozandó hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efa61-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="efa61-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa61-125">-ResourceGroupName</span></span>
<span data-ttu-id="efa61-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efa61-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="efa61-127">Ez a parancsmag létrehoz egy hálózati biztonsági csoportot a paraméter által megadott erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="efa61-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="efa61-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="efa61-128">-SecurityRules</span></span>
<span data-ttu-id="efa61-129">A hálózati biztonsági szabályokban létrehozott objektumok listáját adja meg, amelyek egy hálózati biztonsági csoportban hozhatók létre.</span><span class="sxs-lookup"><span data-stu-id="efa61-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa61-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="efa61-130">-Tag</span></span>
<span data-ttu-id="efa61-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="efa61-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="efa61-132">Példa:</span><span class="sxs-lookup"><span data-stu-id="efa61-132">For example:</span></span>

<span data-ttu-id="efa61-133">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="efa61-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="efa61-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="efa61-134">-Confirm</span></span>
<span data-ttu-id="efa61-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="efa61-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa61-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa61-136">-WhatIf</span></span>
<span data-ttu-id="efa61-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="efa61-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa61-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efa61-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa61-139">CommonParameters</span></span>
<span data-ttu-id="efa61-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efa61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa61-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa61-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa61-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa61-142">INPUTS</span></span>

### <span data-ttu-id="efa61-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="efa61-143">None</span></span>
<span data-ttu-id="efa61-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="efa61-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efa61-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa61-145">OUTPUTS</span></span>

### <span data-ttu-id="efa61-146">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa61-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="efa61-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efa61-147">NOTES</span></span>

## <span data-ttu-id="efa61-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efa61-148">RELATED LINKS</span></span>

[<span data-ttu-id="efa61-149">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa61-149">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="efa61-150">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa61-150">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="efa61-151">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa61-151">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
