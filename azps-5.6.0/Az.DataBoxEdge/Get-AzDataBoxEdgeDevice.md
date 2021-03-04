---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: f02cda5fe04ed72a5e6defd382c372b40c9c039b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942642"
---
# <span data-ttu-id="c3e11-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c3e11-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c3e11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e11-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e11-103">Információkat kap az elérhető Data Box Edge-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="c3e11-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="c3e11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3e11-104">SYNTAX</span></span>

### <span data-ttu-id="c3e11-105">ListByParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3e11-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e11-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e11-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e11-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e11-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e11-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e11-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e11-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e11-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e11-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e11-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e11-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e11-116">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3e11-116">DESCRIPTION</span></span>
<span data-ttu-id="c3e11-117">A **Get-AzDataBoxEdgeDevice** parancsmag az elérhető Data Box Edge-eszközökhöz nyújt információkat.</span><span class="sxs-lookup"><span data-stu-id="c3e11-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="c3e11-118">Az eszköz nevét az Erőforráscsoport neve csoportnévvel együtt megadhatja, hogy az információk egy adott eszközre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="c3e11-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="c3e11-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3e11-119">EXAMPLES</span></span>

### <span data-ttu-id="c3e11-120">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3e11-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="c3e11-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3e11-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="c3e11-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="c3e11-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="c3e11-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3e11-123">PARAMETERS</span></span>

### <span data-ttu-id="c3e11-124">-Alert</span><span class="sxs-lookup"><span data-stu-id="c3e11-124">-Alert</span></span>
<span data-ttu-id="c3e11-125">Az adatmező szélén/átjáróeszközén található értesítések lehívása</span><span class="sxs-lookup"><span data-stu-id="c3e11-125">Fetch the alerts on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="c3e11-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e11-126">-DefaultProfile</span></span>
<span data-ttu-id="c3e11-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3e11-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e11-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="c3e11-128">-ExtendedInfo</span></span>
<span data-ttu-id="c3e11-129">További információ a megadott Data Box Edge/Data Box Átjáró eszközről</span><span class="sxs-lookup"><span data-stu-id="c3e11-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="c3e11-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c3e11-130">-Name</span></span>
<span data-ttu-id="c3e11-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c3e11-131">Resource Group Name</span></span>

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

### <span data-ttu-id="c3e11-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="c3e11-132">-NetworkSetting</span></span>
<span data-ttu-id="c3e11-133">A megadott Data Box Edge/Data Box Átjáró eszköz hálózati beállításainak lekérte</span><span class="sxs-lookup"><span data-stu-id="c3e11-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="c3e11-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e11-134">-ResourceGroupName</span></span>
<span data-ttu-id="c3e11-135">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c3e11-135">Resource Group Name</span></span>

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

### <span data-ttu-id="c3e11-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e11-136">-ResourceId</span></span>
<span data-ttu-id="c3e11-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e11-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="c3e11-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="c3e11-138">-UpdateSummary</span></span>
<span data-ttu-id="c3e11-139">Információkat kap a frissítések elérhetőségéről az eszköz legutóbbi vizsgálatának alapján.</span><span class="sxs-lookup"><span data-stu-id="c3e11-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="c3e11-140">Emellett információkat kap az eszközön folyamatban lévő letöltési vagy telepítési feladatokról is.</span><span class="sxs-lookup"><span data-stu-id="c3e11-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="c3e11-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e11-141">CommonParameters</span></span>
<span data-ttu-id="c3e11-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e11-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e11-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3e11-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e11-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3e11-144">INPUTS</span></span>

### <span data-ttu-id="c3e11-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="c3e11-145">None</span></span>

## <span data-ttu-id="c3e11-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3e11-146">OUTPUTS</span></span>

### <span data-ttu-id="c3e11-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c3e11-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="c3e11-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="c3e11-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="c3e11-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="c3e11-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="c3e11-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="c3e11-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="c3e11-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="c3e11-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="c3e11-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3e11-152">NOTES</span></span>

## <span data-ttu-id="c3e11-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3e11-153">RELATED LINKS</span></span>
