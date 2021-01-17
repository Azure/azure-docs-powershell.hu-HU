---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330354"
---
# <span data-ttu-id="23712-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="23712-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="23712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23712-102">SYNOPSIS</span></span>
<span data-ttu-id="23712-103">Információkat kap az elérhető Data Box Edge-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="23712-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="23712-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23712-104">SYNTAX</span></span>

### <span data-ttu-id="23712-105">ListByParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23712-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23712-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23712-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23712-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23712-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23712-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23712-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23712-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23712-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23712-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23712-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="23712-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23712-116">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23712-116">DESCRIPTION</span></span>
<span data-ttu-id="23712-117">A **Get-AzDataBoxEdgeDevice** parancsmag az elérhető Data Box Edge-eszközökhöz nyújt információkat.</span><span class="sxs-lookup"><span data-stu-id="23712-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="23712-118">Az eszköz nevét az Erőforráscsoport neve csoportnévvel együtt megadhatja, hogy az információk egy adott eszközre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="23712-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="23712-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23712-119">EXAMPLES</span></span>

### <span data-ttu-id="23712-120">1. példa</span><span class="sxs-lookup"><span data-stu-id="23712-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="23712-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="23712-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="23712-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="23712-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="23712-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23712-123">PARAMETERS</span></span>

### <span data-ttu-id="23712-124">-Alert</span><span class="sxs-lookup"><span data-stu-id="23712-124">-Alert</span></span>
<span data-ttu-id="23712-125">Az adatmező szélén/átjáróeszközén található értesítések lehívása</span><span class="sxs-lookup"><span data-stu-id="23712-125">Fetch the alerts on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="23712-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23712-126">-DefaultProfile</span></span>
<span data-ttu-id="23712-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23712-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23712-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="23712-128">-ExtendedInfo</span></span>
<span data-ttu-id="23712-129">További információ a megadott Data Box Edge/Data Box Átjáró eszközről</span><span class="sxs-lookup"><span data-stu-id="23712-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="23712-130">-Name</span><span class="sxs-lookup"><span data-stu-id="23712-130">-Name</span></span>
<span data-ttu-id="23712-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="23712-131">Resource Group Name</span></span>

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

### <span data-ttu-id="23712-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="23712-132">-NetworkSetting</span></span>
<span data-ttu-id="23712-133">A megadott Data Box Edge/Data Box Átjáró eszköz hálózati beállításainak lekérte</span><span class="sxs-lookup"><span data-stu-id="23712-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="23712-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23712-134">-ResourceGroupName</span></span>
<span data-ttu-id="23712-135">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="23712-135">Resource Group Name</span></span>

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

### <span data-ttu-id="23712-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23712-136">-ResourceId</span></span>
<span data-ttu-id="23712-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="23712-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="23712-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="23712-138">-UpdateSummary</span></span>
<span data-ttu-id="23712-139">Információkat kap a frissítések elérhetőségéről az eszköz legutóbbi vizsgálatának alapján.</span><span class="sxs-lookup"><span data-stu-id="23712-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="23712-140">Emellett információkat kap az eszközön folyamatban lévő letöltési vagy telepítési feladatokról is.</span><span class="sxs-lookup"><span data-stu-id="23712-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="23712-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23712-141">CommonParameters</span></span>
<span data-ttu-id="23712-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23712-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23712-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23712-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23712-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23712-144">INPUTS</span></span>

### <span data-ttu-id="23712-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="23712-145">None</span></span>

## <span data-ttu-id="23712-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23712-146">OUTPUTS</span></span>

### <span data-ttu-id="23712-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="23712-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="23712-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="23712-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="23712-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="23712-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="23712-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="23712-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="23712-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="23712-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="23712-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23712-152">NOTES</span></span>

## <span data-ttu-id="23712-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23712-153">RELATED LINKS</span></span>
