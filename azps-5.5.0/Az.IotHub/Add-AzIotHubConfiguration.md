---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: d84d5b172d1a22880b508f8b43f071d5d454cf38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163490"
---
# <span data-ttu-id="1af48-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="1af48-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="1af48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af48-102">SYNOPSIS</span></span>
<span data-ttu-id="1af48-103">IoT automatikus eszközkezelési konfiguráció hozzáadása egy cél IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="1af48-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="1af48-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1af48-104">SYNTAX</span></span>

### <span data-ttu-id="1af48-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1af48-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af48-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1af48-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af48-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1af48-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af48-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1af48-108">DESCRIPTION</span></span>
<span data-ttu-id="1af48-109">A konfigurációs tartalom json és kissé eltér az eszköz vagy a modul szándéka szerint.</span><span class="sxs-lookup"><span data-stu-id="1af48-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="1af48-110">Az eszközkonfigurációk a következő alakban állnak: {"deviceContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="1af48-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="1af48-111">A modulkonfigurációk a következő alakban állnak: {"moduleContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="1af48-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="1af48-112">A konfigurációk a felhasználó által megadott, igény szerinti értékeléshez megadott metrikák alapján definiálhatóak.</span><span class="sxs-lookup"><span data-stu-id="1af48-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="1af48-113">A felhasználói metrikák: json és {"queries":{...}}</span><span class="sxs-lookup"><span data-stu-id="1af48-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="1af48-114">vagy {"metrikák":{"lekérdezések":{...}}}.</span><span class="sxs-lookup"><span data-stu-id="1af48-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="1af48-115">Megjegyzés: A modulok célszabad feltételének "az devices.modules where" kezdettől kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="1af48-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="1af48-116">További https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="1af48-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="1af48-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1af48-117">EXAMPLES</span></span>

### <span data-ttu-id="1af48-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="1af48-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="1af48-119">Eszközkonfiguráció létrehozása alapértelmezett metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="1af48-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="1af48-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="1af48-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="1af48-121">Hozzon létre egy 3-as prioritású eszközkonfigurációt, amely akkor alkalmazható feltétellel, ha egy eszközt címkéznek a 9-es épületben, és a környezet "teszt".</span><span class="sxs-lookup"><span data-stu-id="1af48-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="1af48-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="1af48-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="1af48-123">Felhasználói metrikákat használó eszközkonfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="1af48-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="1af48-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="1af48-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="1af48-125">Hozzon létre címkével egy eszközkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="1af48-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="1af48-126">5. példa</span><span class="sxs-lookup"><span data-stu-id="1af48-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="1af48-127">Hozzon létre tartalommal egy eszközkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="1af48-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="1af48-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1af48-128">PARAMETERS</span></span>

### <span data-ttu-id="1af48-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af48-129">-DefaultProfile</span></span>
<span data-ttu-id="1af48-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1af48-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af48-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="1af48-131">-DeviceContent</span></span>
<span data-ttu-id="1af48-132">Konfiguráció iotHub-eszközökhöz.</span><span class="sxs-lookup"><span data-stu-id="1af48-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="1af48-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af48-133">-InputObject</span></span>
<span data-ttu-id="1af48-134">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="1af48-134">IotHub object</span></span>

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

### <span data-ttu-id="1af48-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1af48-135">-IotHubName</span></span>
<span data-ttu-id="1af48-136">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="1af48-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1af48-137">-Label</span><span class="sxs-lookup"><span data-stu-id="1af48-137">-Label</span></span>
<span data-ttu-id="1af48-138">A célkonfigurációhoz alkalmazandó címkék térképe.</span><span class="sxs-lookup"><span data-stu-id="1af48-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="1af48-139">-Metric</span><span class="sxs-lookup"><span data-stu-id="1af48-139">-Metric</span></span>
<span data-ttu-id="1af48-140">A konfigurációs metrikák definíciójának lekérdezésgyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="1af48-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="1af48-141">-Name</span><span class="sxs-lookup"><span data-stu-id="1af48-141">-Name</span></span>
<span data-ttu-id="1af48-142">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1af48-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="1af48-143">-Priority</span><span class="sxs-lookup"><span data-stu-id="1af48-143">-Priority</span></span>
<span data-ttu-id="1af48-144">Az eszköz konfigurációjának súlya versenyben álló szabályok (legnagyobb nyeremények) esetén.</span><span class="sxs-lookup"><span data-stu-id="1af48-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="1af48-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af48-145">-ResourceGroupName</span></span>
<span data-ttu-id="1af48-146">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1af48-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1af48-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af48-147">-ResourceId</span></span>
<span data-ttu-id="1af48-148">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1af48-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1af48-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="1af48-149">-TargetCondition</span></span>
<span data-ttu-id="1af48-150">Cél feltétel, amelyre az eszközkonfiguráció érvényes.</span><span class="sxs-lookup"><span data-stu-id="1af48-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="1af48-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1af48-151">-Confirm</span></span>
<span data-ttu-id="1af48-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1af48-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af48-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af48-153">-WhatIf</span></span>
<span data-ttu-id="1af48-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1af48-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af48-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1af48-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af48-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af48-156">CommonParameters</span></span>
<span data-ttu-id="1af48-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af48-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af48-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af48-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af48-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1af48-159">INPUTS</span></span>

### <span data-ttu-id="1af48-160">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1af48-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1af48-161">System.String</span><span class="sxs-lookup"><span data-stu-id="1af48-161">System.String</span></span>

## <span data-ttu-id="1af48-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1af48-162">OUTPUTS</span></span>

### <span data-ttu-id="1af48-163">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="1af48-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="1af48-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1af48-164">NOTES</span></span>

## <span data-ttu-id="1af48-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1af48-165">RELATED LINKS</span></span>
