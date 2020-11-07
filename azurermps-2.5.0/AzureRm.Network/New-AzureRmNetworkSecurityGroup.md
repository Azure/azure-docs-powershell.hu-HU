---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 3603adcce2ce39cc4e0a2dd57869a6ca10c48998
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849601"
---
# <span data-ttu-id="0a30f-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a30f-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a30f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a30f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a30f-103">Hálózati biztonsági csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a30f-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a30f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a30f-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a30f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a30f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a30f-106">A **New-AzureRmNetworkSecurityGroup** parancsmag az Azure hálózat biztonsági csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0a30f-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="0a30f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0a30f-107">EXAMPLES</span></span>

### <span data-ttu-id="0a30f-108">1: új hálózati biztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a30f-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="0a30f-109">Ez a parancs létrehoz egy új Azure-hálózati biztonsági csoportot a "nsg1" nevű erőforráscsoport "rg1" nevű erőforráscsoport "westus" nevű csoportjában.</span><span class="sxs-lookup"><span data-stu-id="0a30f-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="0a30f-110">2: részletes hálózati biztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a30f-110">2: Create a detailed network security group</span></span>
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

<span data-ttu-id="0a30f-111">Lépés: 1 biztonsági szabály létrehozása az internetről a 3389-as portra való hozzáférés engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="0a30f-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="0a30f-112">Lépés: 2 biztonsági szabály létrehozása, amely lehetővé teszi az internetről a 80-as port elérését.</span><span class="sxs-lookup"><span data-stu-id="0a30f-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="0a30f-113">Lépés: 3 vegye fel a fentiek alapján létrehozott szabályokat egy NSG-FrontEnd nevű új NSG.</span><span class="sxs-lookup"><span data-stu-id="0a30f-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="0a30f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a30f-114">PARAMETERS</span></span>

### <span data-ttu-id="0a30f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a30f-115">-AsJob</span></span>
<span data-ttu-id="0a30f-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0a30f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a30f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a30f-117">-DefaultProfile</span></span>
<span data-ttu-id="0a30f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a30f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a30f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0a30f-119">-Force</span></span>
<span data-ttu-id="0a30f-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0a30f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a30f-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="0a30f-121">-Location</span></span>
<span data-ttu-id="0a30f-122">Azt a régiót adja meg, amelyhez hálózati biztonsági csoportot szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="0a30f-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="0a30f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a30f-123">-Name</span></span>
<span data-ttu-id="0a30f-124">A létrehozandó hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a30f-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="0a30f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a30f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a30f-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a30f-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0a30f-127">Ez a parancsmag létrehoz egy hálózati biztonsági csoportot a paraméter által megadott erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="0a30f-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0a30f-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="0a30f-128">-SecurityRules</span></span>
<span data-ttu-id="0a30f-129">A hálózati biztonsági szabályokban létrehozott objektumok listáját adja meg, amelyek egy hálózati biztonsági csoportban hozhatók létre.</span><span class="sxs-lookup"><span data-stu-id="0a30f-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="0a30f-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="0a30f-130">-Tag</span></span>
<span data-ttu-id="0a30f-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0a30f-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a30f-132">Példa:</span><span class="sxs-lookup"><span data-stu-id="0a30f-132">For example:</span></span>

<span data-ttu-id="0a30f-133">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0a30f-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0a30f-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a30f-134">-Confirm</span></span>
<span data-ttu-id="0a30f-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a30f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a30f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a30f-136">-WhatIf</span></span>
<span data-ttu-id="0a30f-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a30f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a30f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a30f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a30f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a30f-139">CommonParameters</span></span>
<span data-ttu-id="0a30f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a30f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a30f-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a30f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a30f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a30f-142">INPUTS</span></span>

## <span data-ttu-id="0a30f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a30f-143">OUTPUTS</span></span>

### <span data-ttu-id="0a30f-144">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a30f-144">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a30f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a30f-145">NOTES</span></span>

## <span data-ttu-id="0a30f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a30f-146">RELATED LINKS</span></span>

[<span data-ttu-id="0a30f-147">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a30f-147">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0a30f-148">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a30f-148">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0a30f-149">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a30f-149">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
