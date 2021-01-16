---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470221"
---
# <span data-ttu-id="ccc42-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ccc42-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="ccc42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccc42-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc42-103">Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="ccc42-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="ccc42-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ccc42-104">SYNTAX</span></span>

### <span data-ttu-id="ccc42-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="ccc42-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccc42-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="ccc42-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccc42-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ccc42-107">DESCRIPTION</span></span>
<span data-ttu-id="ccc42-108">A helyi hálózati átjáró a virtuális magánhálózati eszköz helyszíni objektumának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="ccc42-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="ccc42-109">A **New-AzLocalNetworkGateway** parancsmag létrehozza a helyszíni átjárónak megfelelő objektumot az átjáró neve, erőforráscsoportneve, helye és IP-címe, valamint az Azure-hoz csatlakozó helyszíni hálózat címelőtagja alapján.</span><span class="sxs-lookup"><span data-stu-id="ccc42-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="ccc42-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ccc42-110">EXAMPLES</span></span>

### <span data-ttu-id="ccc42-111">1. példa: Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="ccc42-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="ccc42-112">Létrehozza a helyi hálózati átjáró "myLocalGW" nevű objektumát a "myRG" erőforráscsoportban a "Nyugat-USA" helyen a "23.99.221.164" IP-címmel és a "10.5.51.0/24" előtaggal a helyszínen.</span><span class="sxs-lookup"><span data-stu-id="ccc42-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="ccc42-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccc42-113">PARAMETERS</span></span>

### <span data-ttu-id="ccc42-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ccc42-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="ccc42-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccc42-115">-AsJob</span></span>
<span data-ttu-id="ccc42-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ccc42-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccc42-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="ccc42-117">-Asn</span></span>
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

### <span data-ttu-id="ccc42-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ccc42-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="ccc42-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc42-119">-DefaultProfile</span></span>
<span data-ttu-id="ccc42-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccc42-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccc42-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ccc42-121">-Force</span></span>
<span data-ttu-id="ccc42-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ccc42-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ccc42-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="ccc42-123">-Fqdn</span></span>
<span data-ttu-id="ccc42-124">A helyi hálózati átjáró teljes tartománya.</span><span class="sxs-lookup"><span data-stu-id="ccc42-124">FQDN of local network gateway.</span></span>

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

### <span data-ttu-id="ccc42-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="ccc42-125">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="ccc42-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ccc42-126">-Location</span></span>
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

### <span data-ttu-id="ccc42-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ccc42-127">-Name</span></span>
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

### <span data-ttu-id="ccc42-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ccc42-128">-PeerWeight</span></span>
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

### <span data-ttu-id="ccc42-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc42-129">-ResourceGroupName</span></span>
<span data-ttu-id="ccc42-130">Azt az erőforráscsoportot adja meg, amelyhez a helyi hálózati átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="ccc42-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="ccc42-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ccc42-131">-Tag</span></span>
<span data-ttu-id="ccc42-132">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="ccc42-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ccc42-133">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="ccc42-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ccc42-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccc42-134">-Confirm</span></span>
<span data-ttu-id="ccc42-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ccc42-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccc42-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccc42-136">-WhatIf</span></span>
<span data-ttu-id="ccc42-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ccc42-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccc42-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccc42-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccc42-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc42-139">CommonParameters</span></span>
<span data-ttu-id="ccc42-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc42-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc42-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccc42-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc42-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccc42-142">INPUTS</span></span>

### <span data-ttu-id="ccc42-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ccc42-143">System.String</span></span>

### <span data-ttu-id="ccc42-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ccc42-144">System.String[]</span></span>

### <span data-ttu-id="ccc42-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="ccc42-145">System.UInt32</span></span>

### <span data-ttu-id="ccc42-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ccc42-146">System.Int32</span></span>

### <span data-ttu-id="ccc42-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ccc42-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ccc42-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc42-148">OUTPUTS</span></span>

### <span data-ttu-id="ccc42-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ccc42-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ccc42-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ccc42-150">NOTES</span></span>

## <span data-ttu-id="ccc42-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccc42-151">RELATED LINKS</span></span>

[<span data-ttu-id="ccc42-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ccc42-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="ccc42-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ccc42-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="ccc42-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ccc42-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
