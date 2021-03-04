---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 2521d73d26b281e2dbc242e860869e4e31c78208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942553"
---
# <span data-ttu-id="448a4-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="448a4-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="448a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448a4-102">SYNOPSIS</span></span>
<span data-ttu-id="448a4-103">IoT automatikus eszközkezelési konfiguráció hozzáadása egy cél IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="448a4-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="448a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="448a4-104">SYNTAX</span></span>

### <span data-ttu-id="448a4-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="448a4-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448a4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="448a4-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="448a4-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="448a4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="448a4-108">DESCRIPTION</span></span>
<span data-ttu-id="448a4-109">A konfigurációs tartalom json és kissé eltér az eszköz vagy a modul szándéka szerint.</span><span class="sxs-lookup"><span data-stu-id="448a4-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="448a4-110">Az eszközkonfigurációk a következő alakban állnak: {"deviceContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="448a4-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="448a4-111">A modulkonfigurációk a következő alakban állnak: {"moduleContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="448a4-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="448a4-112">A konfigurációk a felhasználó által megadott, igény szerinti értékeléshez megadott metrikák alapján definiálhatóak.</span><span class="sxs-lookup"><span data-stu-id="448a4-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="448a4-113">A felhasználói metrikák: json és {"queries":{...}}</span><span class="sxs-lookup"><span data-stu-id="448a4-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="448a4-114">vagy {"metrikák":{"lekérdezések":{...}}}.</span><span class="sxs-lookup"><span data-stu-id="448a4-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="448a4-115">Megjegyzés: A modulok célszabad feltételének "az devices.modules where" kezdettől kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="448a4-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="448a4-116">További https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="448a4-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="448a4-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="448a4-117">EXAMPLES</span></span>

### <span data-ttu-id="448a4-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="448a4-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="448a4-119">Alapértelmezett metaadatokkal is létrehozhat eszközkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="448a4-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="448a4-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="448a4-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="448a4-121">Hozzon létre egy 3-as prioritású eszközkonfigurációt, amely akkor alkalmazható feltétellel, ha egy eszközt címkéznek a 9-es épületben, és a környezet "teszt".</span><span class="sxs-lookup"><span data-stu-id="448a4-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="448a4-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="448a4-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="448a4-123">Felhasználói metrikákat használó eszközkonfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="448a4-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="448a4-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="448a4-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="448a4-125">Hozzon létre címkével egy eszközkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="448a4-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="448a4-126">5. példa</span><span class="sxs-lookup"><span data-stu-id="448a4-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="448a4-127">Hozzon létre tartalommal egy eszközkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="448a4-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="448a4-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="448a4-128">PARAMETERS</span></span>

### <span data-ttu-id="448a4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448a4-129">-DefaultProfile</span></span>
<span data-ttu-id="448a4-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="448a4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="448a4-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="448a4-131">-DeviceContent</span></span>
<span data-ttu-id="448a4-132">Konfiguráció iotHub-eszközökhöz.</span><span class="sxs-lookup"><span data-stu-id="448a4-132">Configuration for IotHub devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="448a4-133">-InputObject</span></span>
<span data-ttu-id="448a4-134">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="448a4-134">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="448a4-135">-IotHubName</span></span>
<span data-ttu-id="448a4-136">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="448a4-136">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-137">-Label</span><span class="sxs-lookup"><span data-stu-id="448a4-137">-Label</span></span>
<span data-ttu-id="448a4-138">A célkonfigurációhoz alkalmazandó címkék térképe.</span><span class="sxs-lookup"><span data-stu-id="448a4-138">Map of labels to be applied to target configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-139">-Metric</span><span class="sxs-lookup"><span data-stu-id="448a4-139">-Metric</span></span>
<span data-ttu-id="448a4-140">A konfigurációs metrikák definíciójának lekérdezésgyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="448a4-140">Queries collection for configuration metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-141">-Name</span><span class="sxs-lookup"><span data-stu-id="448a4-141">-Name</span></span>
<span data-ttu-id="448a4-142">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="448a4-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="448a4-143">-Priority</span><span class="sxs-lookup"><span data-stu-id="448a4-143">-Priority</span></span>
<span data-ttu-id="448a4-144">Az eszköz konfigurációjának súlya versenyben álló szabályok (legnagyobb nyeremények) esetén.</span><span class="sxs-lookup"><span data-stu-id="448a4-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448a4-145">-ResourceGroupName</span></span>
<span data-ttu-id="448a4-146">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="448a4-146">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="448a4-147">-ResourceId</span></span>
<span data-ttu-id="448a4-148">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="448a4-148">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="448a4-149">-TargetCondition</span></span>
<span data-ttu-id="448a4-150">Cél feltétel, amelyre az eszközkonfiguráció érvényes.</span><span class="sxs-lookup"><span data-stu-id="448a4-150">Target condition in which a device configuration applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448a4-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="448a4-151">-Confirm</span></span>
<span data-ttu-id="448a4-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="448a4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="448a4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448a4-153">-WhatIf</span></span>
<span data-ttu-id="448a4-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="448a4-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="448a4-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="448a4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="448a4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448a4-156">CommonParameters</span></span>
<span data-ttu-id="448a4-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="448a4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448a4-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448a4-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448a4-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="448a4-159">INPUTS</span></span>

### <span data-ttu-id="448a4-160">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="448a4-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="448a4-161">System.String</span><span class="sxs-lookup"><span data-stu-id="448a4-161">System.String</span></span>

## <span data-ttu-id="448a4-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="448a4-162">OUTPUTS</span></span>

### <span data-ttu-id="448a4-163">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="448a4-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="448a4-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="448a4-164">NOTES</span></span>

## <span data-ttu-id="448a4-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="448a4-165">RELATED LINKS</span></span>
