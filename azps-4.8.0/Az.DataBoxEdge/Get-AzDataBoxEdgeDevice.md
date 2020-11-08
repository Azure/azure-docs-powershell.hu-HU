---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185056"
---
# <span data-ttu-id="91b6c-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="91b6c-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="91b6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="91b6c-103">A rendelkezésre álló adatok mező Edge-eszközökről kapja meg az információkat.</span><span class="sxs-lookup"><span data-stu-id="91b6c-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="91b6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91b6c-104">SYNTAX</span></span>

### <span data-ttu-id="91b6c-105">ListByParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91b6c-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91b6c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b6c-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91b6c-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91b6c-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91b6c-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91b6c-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b6c-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b6c-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b6c-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b6c-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6c-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b6c-116">Leírás</span><span class="sxs-lookup"><span data-stu-id="91b6c-116">DESCRIPTION</span></span>
<span data-ttu-id="91b6c-117">A **Get-AzDataBoxEdgeDevice** parancsmag információkat kap az elérhető adatmező Edge-eszközökről.</span><span class="sxs-lookup"><span data-stu-id="91b6c-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="91b6c-118">Az eszköz nevét az erőforráscsoport nevével együtt megadhatja, ha egy adott eszközön szeretne információt kapni.</span><span class="sxs-lookup"><span data-stu-id="91b6c-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="91b6c-119">Példák</span><span class="sxs-lookup"><span data-stu-id="91b6c-119">EXAMPLES</span></span>

### <span data-ttu-id="91b6c-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91b6c-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="91b6c-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="91b6c-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="91b6c-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="91b6c-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="91b6c-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91b6c-123">PARAMETERS</span></span>

### <span data-ttu-id="91b6c-124">-Értesítés</span><span class="sxs-lookup"><span data-stu-id="91b6c-124">-Alert</span></span>
<span data-ttu-id="91b6c-125">Értesítések beolvasása az adatmező szélén/átjáró eszközön</span><span class="sxs-lookup"><span data-stu-id="91b6c-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b6c-126">-DefaultProfile</span></span>
<span data-ttu-id="91b6c-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91b6c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91b6c-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="91b6c-128">-ExtendedInfo</span></span>
<span data-ttu-id="91b6c-129">További információ kérése a megadott adatok mező Edge/Data Box Gateway eszközéhez</span><span class="sxs-lookup"><span data-stu-id="91b6c-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b6c-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91b6c-130">-Name</span></span>
<span data-ttu-id="91b6c-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="91b6c-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b6c-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="91b6c-132">-NetworkSetting</span></span>
<span data-ttu-id="91b6c-133">A megadott adatmező Edge/Data Box Gateway eszköz hálózati beállításainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="91b6c-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b6c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b6c-134">-ResourceGroupName</span></span>
<span data-ttu-id="91b6c-135">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="91b6c-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b6c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91b6c-136">-ResourceId</span></span>
<span data-ttu-id="91b6c-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="91b6c-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b6c-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="91b6c-138">-UpdateSummary</span></span>
<span data-ttu-id="91b6c-139">Információkat kaphat az eszköz utolsó vizsgálatán alapuló frissítések elérhetőségéről.</span><span class="sxs-lookup"><span data-stu-id="91b6c-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="91b6c-140">Az eszközön minden folyamatban lévő letöltési vagy telepítési feladatról is tájékoztatást kap.</span><span class="sxs-lookup"><span data-stu-id="91b6c-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b6c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b6c-141">CommonParameters</span></span>
<span data-ttu-id="91b6c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91b6c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b6c-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91b6c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b6c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91b6c-144">INPUTS</span></span>

### <span data-ttu-id="91b6c-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="91b6c-145">None</span></span>

## <span data-ttu-id="91b6c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91b6c-146">OUTPUTS</span></span>

### <span data-ttu-id="91b6c-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="91b6c-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="91b6c-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="91b6c-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="91b6c-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="91b6c-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="91b6c-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="91b6c-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="91b6c-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="91b6c-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="91b6c-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91b6c-152">NOTES</span></span>

## <span data-ttu-id="91b6c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91b6c-153">RELATED LINKS</span></span>
