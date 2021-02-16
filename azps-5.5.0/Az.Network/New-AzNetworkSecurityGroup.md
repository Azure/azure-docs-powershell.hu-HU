---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202774"
---
# <span data-ttu-id="938f4-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="938f4-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="938f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="938f4-102">SYNOPSIS</span></span>
<span data-ttu-id="938f4-103">Hálózati biztonsági csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="938f4-103">Creates a network security group.</span></span>

## <span data-ttu-id="938f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="938f4-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="938f4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="938f4-105">DESCRIPTION</span></span>
<span data-ttu-id="938f4-106">A **New-AzNetworkSecurityGroup** parancsmag létrehoz egy Azure-hálózat biztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="938f4-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="938f4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="938f4-107">EXAMPLES</span></span>

### <span data-ttu-id="938f4-108">1. példa: Új hálózatbiztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="938f4-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="938f4-109">Ez a parancs létrehoz egy "nsg1" nevű új Azure-hálózatbiztonsági csoportot az "rg1" erőforráscsoportban a "westus" helyen.</span><span class="sxs-lookup"><span data-stu-id="938f4-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="938f4-110">2. példa: Részletes hálózatbiztonsági csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="938f4-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="938f4-111">Lépés:1 Hozzon létre egy olyan biztonsági szabályt, amely engedélyezi az internetről a 3389-es portot.</span><span class="sxs-lookup"><span data-stu-id="938f4-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="938f4-112">Lépés:2 Hozzon létre egy olyan biztonsági szabályt, amely engedélyezi az internetről való hozzáférést a 80-as porthoz.</span><span class="sxs-lookup"><span data-stu-id="938f4-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="938f4-113">Lépés:3 Adja hozzá a fent létrehozott szabályokat egy NSG-FrontEnd nevű új NSG-hez.</span><span class="sxs-lookup"><span data-stu-id="938f4-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="938f4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="938f4-114">PARAMETERS</span></span>

### <span data-ttu-id="938f4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="938f4-115">-AsJob</span></span>
<span data-ttu-id="938f4-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="938f4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="938f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="938f4-117">-DefaultProfile</span></span>
<span data-ttu-id="938f4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="938f4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="938f4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="938f4-119">-Force</span></span>
<span data-ttu-id="938f4-120">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="938f4-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="938f4-121">-Location</span><span class="sxs-lookup"><span data-stu-id="938f4-121">-Location</span></span>
<span data-ttu-id="938f4-122">Azt a régiót adja meg, amelyhez hálózati biztonsági csoportot kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="938f4-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="938f4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="938f4-123">-Name</span></span>
<span data-ttu-id="938f4-124">A létrehozni szükséges hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="938f4-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="938f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="938f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="938f4-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="938f4-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="938f4-127">Ez a parancsmag létrehoz egy hálózati biztonsági csoportot a paraméter által megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="938f4-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="938f4-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="938f4-128">-SecurityRules</span></span>
<span data-ttu-id="938f4-129">Megadja a hálózati biztonsági csoportokban létrehozható hálózati biztonsági szabályobjektumok listáját.</span><span class="sxs-lookup"><span data-stu-id="938f4-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="938f4-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="938f4-130">-Tag</span></span>
<span data-ttu-id="938f4-131">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="938f4-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="938f4-132">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="938f4-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="938f4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="938f4-133">-Confirm</span></span>
<span data-ttu-id="938f4-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="938f4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="938f4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="938f4-135">-WhatIf</span></span>
<span data-ttu-id="938f4-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="938f4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="938f4-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="938f4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="938f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="938f4-138">CommonParameters</span></span>
<span data-ttu-id="938f4-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="938f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="938f4-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="938f4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="938f4-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="938f4-141">INPUTS</span></span>

### <span data-ttu-id="938f4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="938f4-142">System.String</span></span>

### <span data-ttu-id="938f4-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="938f4-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="938f4-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="938f4-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="938f4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="938f4-145">OUTPUTS</span></span>

### <span data-ttu-id="938f4-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="938f4-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="938f4-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="938f4-147">NOTES</span></span>

## <span data-ttu-id="938f4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="938f4-148">RELATED LINKS</span></span>

[<span data-ttu-id="938f4-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="938f4-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="938f4-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="938f4-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="938f4-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="938f4-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
