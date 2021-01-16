---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334602"
---
# <span data-ttu-id="31501-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31501-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="31501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31501-102">SYNOPSIS</span></span>
<span data-ttu-id="31501-103">Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="31501-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="31501-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31501-104">SYNTAX</span></span>

### <span data-ttu-id="31501-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="31501-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31501-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="31501-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31501-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31501-107">DESCRIPTION</span></span>
<span data-ttu-id="31501-108">A helyi hálózati átjáró a virtuális magánhálózati eszköz helyszíni objektumának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="31501-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="31501-109">A **New-AzLocalNetworkGateway** parancsmag létrehozza a helyszíni átjárónak megfelelő objektumot az átjáró neve, erőforráscsoportneve, helye és IP-címe, valamint az Azure-hoz csatlakozó helyszíni hálózat címelőtagja alapján.</span><span class="sxs-lookup"><span data-stu-id="31501-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="31501-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31501-110">EXAMPLES</span></span>

### <span data-ttu-id="31501-111">1. példa: Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="31501-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="31501-112">Létrehozza a helyi hálózati átjáró "myLocalGW" nevű objektumát a "myRG" erőforráscsoportban a "Nyugat-USA" helyen a "23.99.221.164" IP-címmel és a "10.5.51.0/24" előtaggal a helyszínen.</span><span class="sxs-lookup"><span data-stu-id="31501-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="31501-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31501-113">PARAMETERS</span></span>

### <span data-ttu-id="31501-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="31501-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31501-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31501-115">-AsJob</span></span>
<span data-ttu-id="31501-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="31501-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31501-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="31501-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31501-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="31501-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31501-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31501-119">-DefaultProfile</span></span>
<span data-ttu-id="31501-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31501-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31501-121">-Force</span><span class="sxs-lookup"><span data-stu-id="31501-121">-Force</span></span>
<span data-ttu-id="31501-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="31501-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31501-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="31501-123">-Fqdn</span></span>
<span data-ttu-id="31501-124">A helyi hálózati átjáró teljes tartománya.</span><span class="sxs-lookup"><span data-stu-id="31501-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31501-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="31501-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31501-126">-Location</span><span class="sxs-lookup"><span data-stu-id="31501-126">-Location</span></span>
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

### <span data-ttu-id="31501-127">-Name</span><span class="sxs-lookup"><span data-stu-id="31501-127">-Name</span></span>
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

### <span data-ttu-id="31501-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="31501-128">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31501-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31501-129">-ResourceGroupName</span></span>
<span data-ttu-id="31501-130">Azt az erőforráscsoportot adja meg, amelyhez a helyi hálózati átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="31501-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="31501-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="31501-131">-Tag</span></span>
<span data-ttu-id="31501-132">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="31501-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31501-133">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="31501-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="31501-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31501-134">-Confirm</span></span>
<span data-ttu-id="31501-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="31501-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31501-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31501-136">-WhatIf</span></span>
<span data-ttu-id="31501-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="31501-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31501-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31501-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31501-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31501-139">CommonParameters</span></span>
<span data-ttu-id="31501-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31501-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31501-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31501-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31501-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31501-142">INPUTS</span></span>

### <span data-ttu-id="31501-143">System.String</span><span class="sxs-lookup"><span data-stu-id="31501-143">System.String</span></span>

### <span data-ttu-id="31501-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="31501-144">System.String[]</span></span>

### <span data-ttu-id="31501-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="31501-145">System.UInt32</span></span>

### <span data-ttu-id="31501-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="31501-146">System.Int32</span></span>

### <span data-ttu-id="31501-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="31501-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="31501-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31501-148">OUTPUTS</span></span>

### <span data-ttu-id="31501-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31501-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="31501-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31501-150">NOTES</span></span>

## <span data-ttu-id="31501-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31501-151">RELATED LINKS</span></span>

[<span data-ttu-id="31501-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31501-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="31501-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31501-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="31501-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31501-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
