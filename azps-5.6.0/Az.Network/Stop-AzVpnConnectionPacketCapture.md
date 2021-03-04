---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: d37bd9fa620b6da68c311399be811f639ea85aea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918497"
---
# <span data-ttu-id="11019-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11019-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="11019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11019-102">SYNOPSIS</span></span>
<span data-ttu-id="11019-103">A Csomagrögzítés leállítja a műveletet Vpn-kapcsolaton</span><span class="sxs-lookup"><span data-stu-id="11019-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="11019-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11019-104">SYNTAX</span></span>

### <span data-ttu-id="11019-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11019-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11019-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="11019-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11019-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="11019-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11019-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11019-108">DESCRIPTION</span></span>
<span data-ttu-id="11019-109">Leállítja a csomagrögzítési műveletet Vpn-kapcsolaton, és feltölti az eredményt az adott SasUrl tárolón.</span><span class="sxs-lookup"><span data-stu-id="11019-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="11019-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11019-110">EXAMPLES</span></span>

### <span data-ttu-id="11019-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="11019-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="11019-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="11019-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="11019-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11019-113">PARAMETERS</span></span>

### <span data-ttu-id="11019-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11019-114">-AsJob</span></span>
<span data-ttu-id="11019-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="11019-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11019-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11019-116">-DefaultProfile</span></span>
<span data-ttu-id="11019-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11019-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11019-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11019-118">-InputObject</span></span>
<span data-ttu-id="11019-119">A Vpn-kapcsolatobjektum, amelyben a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="11019-119">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11019-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="11019-120">-LinkConnectionName</span></span>
<span data-ttu-id="11019-121">A SiteLinkConnection nevei.</span><span class="sxs-lookup"><span data-stu-id="11019-121">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11019-122">-Name</span><span class="sxs-lookup"><span data-stu-id="11019-122">-Name</span></span>
<span data-ttu-id="11019-123">A Vpn-kapcsolat neve, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="11019-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11019-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="11019-124">-ParentResourceName</span></span>
<span data-ttu-id="11019-125">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11019-125">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11019-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11019-126">-ResourceGroupName</span></span>
<span data-ttu-id="11019-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11019-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11019-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11019-128">-ResourceId</span></span>
<span data-ttu-id="11019-129">A VpnConnection Azure-erőforrásazonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="11019-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11019-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="11019-130">-SasUrl</span></span>
<span data-ttu-id="11019-131">A Vpn-en a csomagok rögzítésének leállítását lehetővé t tő SAS URL-címe.</span><span class="sxs-lookup"><span data-stu-id="11019-131">SAS Url for stop packet capture on Vpn.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11019-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11019-132">-Confirm</span></span>
<span data-ttu-id="11019-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11019-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11019-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11019-134">-WhatIf</span></span>
<span data-ttu-id="11019-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11019-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11019-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11019-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11019-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11019-137">CommonParameters</span></span>
<span data-ttu-id="11019-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11019-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11019-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11019-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11019-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11019-140">INPUTS</span></span>

### <span data-ttu-id="11019-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="11019-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="11019-142">System.String</span><span class="sxs-lookup"><span data-stu-id="11019-142">System.String</span></span>

## <span data-ttu-id="11019-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11019-143">OUTPUTS</span></span>

### <span data-ttu-id="11019-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="11019-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="11019-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11019-145">NOTES</span></span>

## <span data-ttu-id="11019-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11019-146">RELATED LINKS</span></span>

[<span data-ttu-id="11019-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11019-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)