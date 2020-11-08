---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: 1fa868d9df41a5f4f995981c332497d9555e1174
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011668"
---
# <span data-ttu-id="9c35b-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9c35b-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="9c35b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c35b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c35b-103">A rendelkezésre álló halom Edge-eszközökről kapja meg az információkat.</span><span class="sxs-lookup"><span data-stu-id="9c35b-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="9c35b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c35b-104">SYNTAX</span></span>

### <span data-ttu-id="9c35b-105">ListByParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c35b-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c35b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c35b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c35b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c35b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c35b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c35b-108">DESCRIPTION</span></span>
<span data-ttu-id="9c35b-109">A **Get-AzStackEdgeDevice** parancsmag információkat kap a rendelkezésre álló halom Edge-eszközökről.</span><span class="sxs-lookup"><span data-stu-id="9c35b-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="9c35b-110">Az eszköz nevét az erőforráscsoport nevével együtt megadhatja, ha egy adott eszközön szeretne információt kapni.</span><span class="sxs-lookup"><span data-stu-id="9c35b-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="9c35b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9c35b-111">EXAMPLES</span></span>

### <span data-ttu-id="9c35b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c35b-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="9c35b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9c35b-113">Example 2</span></span>
```powershell
PS C:\>$device = Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName1 -DeviceName deviceNameOne -Alert -UpdateSummary -NetworkSetting -ExtendedInfo

PS C:\>$device.Alert

Title                            Severity AppearedDateTime      Recommendation
-----                            -------- ----------------      --------------
Lost heartbeat from your device. Critical 02-Jan-20 10:35:20 AM If your device is offline, then the device is not able to communicate with the Azure service. This could be due to one of the following reasons: <br/> &nbs�


PS C:\>$device.NetworkSetting

State    IPv4         IPv6                                 Subnet        Default Gateway Physical address DNS Servers
-----    ----         ----                                 ------        --------------- ---------------- -----------
Disabled 10.150.76.82 2404:f801:4800:1e:8168:dca6:b3b9:d70 255.255.252.0 10.150.76.1     00155D4E262B     10.50.50.50,10.50.10.50

PS C:\>$device.UpdateSummary

DeviceName        Current Version Friendly name      Last Software Scan Last Software Update Pending Updates Pending Update Titles
----------        --------------- -------------      ------------------ -------------------- --------------- ---------------------
deviceNameOne     2.0.998.537     Data Box Edge Mock                                         0

PS C:\>$device.ExtendedInfo

ResourceGroupName   DeviceName        EncryptedCIK Thumbprint     ResourceKey        EncryptedCIK
-----------------   ----------        -----------------------     -----------        ------------
resourceGroupName1  deviceNameOne     EncryptedCIKThumbpring      411182691329779166 EncryptedCIK
```

## <span data-ttu-id="9c35b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c35b-114">PARAMETERS</span></span>

### <span data-ttu-id="9c35b-115">-Értesítés</span><span class="sxs-lookup"><span data-stu-id="9c35b-115">-Alert</span></span>
<span data-ttu-id="9c35b-116">Értesítések beolvasása a halom szélén/átjáró eszközön</span><span class="sxs-lookup"><span data-stu-id="9c35b-116">Fetch the alerts on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c35b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c35b-117">-DefaultProfile</span></span>
<span data-ttu-id="9c35b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c35b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c35b-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="9c35b-119">-ExtendedInfo</span></span>
<span data-ttu-id="9c35b-120">További információk a megadott halom Edge/halom átjáró eszközhöz</span><span class="sxs-lookup"><span data-stu-id="9c35b-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c35b-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c35b-121">-Name</span></span>
<span data-ttu-id="9c35b-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9c35b-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c35b-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="9c35b-123">-NetworkSetting</span></span>
<span data-ttu-id="9c35b-124">A megadott halom Edge/halom átjáró eszköz hálózati beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9c35b-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c35b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c35b-125">-ResourceGroupName</span></span>
<span data-ttu-id="9c35b-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9c35b-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c35b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c35b-127">-ResourceId</span></span>
<span data-ttu-id="9c35b-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c35b-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c35b-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="9c35b-129">-UpdateSummary</span></span>
<span data-ttu-id="9c35b-130">Információkat kaphat az eszköz utolsó vizsgálatán alapuló frissítések elérhetőségéről.</span><span class="sxs-lookup"><span data-stu-id="9c35b-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="9c35b-131">Az eszközön minden folyamatban lévő letöltési vagy telepítési feladatról is tájékoztatást kap.</span><span class="sxs-lookup"><span data-stu-id="9c35b-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c35b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c35b-132">CommonParameters</span></span>
<span data-ttu-id="9c35b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c35b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c35b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c35b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c35b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c35b-135">INPUTS</span></span>

## <span data-ttu-id="9c35b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c35b-136">OUTPUTS</span></span>

## <span data-ttu-id="9c35b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c35b-137">NOTES</span></span>

## <span data-ttu-id="9c35b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c35b-138">RELATED LINKS</span></span>
