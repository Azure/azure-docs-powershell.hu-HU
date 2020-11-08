---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187792"
---
# <span data-ttu-id="7144a-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="7144a-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="7144a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7144a-102">SYNOPSIS</span></span>
<span data-ttu-id="7144a-103">IoT automatikus eszközkezelés-konfiguráció felvétele a TARGET IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="7144a-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="7144a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7144a-104">SYNTAX</span></span>

### <span data-ttu-id="7144a-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7144a-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7144a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7144a-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7144a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7144a-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7144a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7144a-108">DESCRIPTION</span></span>
<span data-ttu-id="7144a-109">A konfigurációs tartalmak a JSON és a kis-és nagybetűs szerkezettől függően változhatnak.</span><span class="sxs-lookup"><span data-stu-id="7144a-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="7144a-110">Az eszközök konfigurációi {"deviceContent": {...}} formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="7144a-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="7144a-111">A modul-konfigurációk {"moduleContent": {...}} formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="7144a-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="7144a-112">Az igény szerinti értékeléshez a beállítások a felhasználó által megadott metrikákkal definiálhatók.</span><span class="sxs-lookup"><span data-stu-id="7144a-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="7144a-113">Felhasználói metrikák: JSON és {"lekérdezések" ({...}) formában</span><span class="sxs-lookup"><span data-stu-id="7144a-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="7144a-114">vagy {"metrikus": {"lekérdezések": {...}}.</span><span class="sxs-lookup"><span data-stu-id="7144a-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="7144a-115">Megjegyzés: a modulokban a cél feltételének kell kezdődnie az "eszközökről. modulokból".</span><span class="sxs-lookup"><span data-stu-id="7144a-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="7144a-116"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="7144a-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="7144a-117">Példák</span><span class="sxs-lookup"><span data-stu-id="7144a-117">EXAMPLES</span></span>

### <span data-ttu-id="7144a-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7144a-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="7144a-119">Az alapértelmezett metaadatokat tartalmazó eszköz-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="7144a-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="7144a-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="7144a-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="7144a-121">A 3-as prioritású eszköz-konfigurációt akkor alkalmazza, ha az eszköz a 9-es épületben van megcímkézve, és a környezet "teszt".</span><span class="sxs-lookup"><span data-stu-id="7144a-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="7144a-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="7144a-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="7144a-123">Eszköz-konfiguráció létrehozása felhasználói mérőszámokkal.</span><span class="sxs-lookup"><span data-stu-id="7144a-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="7144a-124">3. példa</span><span class="sxs-lookup"><span data-stu-id="7144a-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="7144a-125">Az eszköz konfigurációjának létrehozása feliratokkal.</span><span class="sxs-lookup"><span data-stu-id="7144a-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="7144a-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="7144a-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="7144a-127">A tartalommal rendelkező eszköz-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="7144a-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="7144a-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7144a-128">PARAMETERS</span></span>

### <span data-ttu-id="7144a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7144a-129">-DefaultProfile</span></span>
<span data-ttu-id="7144a-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7144a-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7144a-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="7144a-131">-DeviceContent</span></span>
<span data-ttu-id="7144a-132">IotHub-eszközök konfigurációja</span><span class="sxs-lookup"><span data-stu-id="7144a-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="7144a-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7144a-133">-InputObject</span></span>
<span data-ttu-id="7144a-134">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="7144a-134">IotHub object</span></span>

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

### <span data-ttu-id="7144a-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7144a-135">-IotHubName</span></span>
<span data-ttu-id="7144a-136">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="7144a-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7144a-137">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="7144a-137">-Label</span></span>
<span data-ttu-id="7144a-138">A cél-konfigurációra alkalmazandó címkék megfeleltetése.</span><span class="sxs-lookup"><span data-stu-id="7144a-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="7144a-139">-Metrikus</span><span class="sxs-lookup"><span data-stu-id="7144a-139">-Metric</span></span>
<span data-ttu-id="7144a-140">Lekérdezések gyűjteménye a konfigurációs metrikák definícióhoz.</span><span class="sxs-lookup"><span data-stu-id="7144a-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="7144a-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7144a-141">-Name</span></span>
<span data-ttu-id="7144a-142">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7144a-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="7144a-143">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="7144a-143">-Priority</span></span>
<span data-ttu-id="7144a-144">Az eszköz konfigurációjának súlya a versengő szabályok (legmagasabb WINS) esetén.</span><span class="sxs-lookup"><span data-stu-id="7144a-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="7144a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7144a-145">-ResourceGroupName</span></span>
<span data-ttu-id="7144a-146">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7144a-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7144a-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7144a-147">-ResourceId</span></span>
<span data-ttu-id="7144a-148">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="7144a-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7144a-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="7144a-149">-TargetCondition</span></span>
<span data-ttu-id="7144a-150">Az a cél feltétel, amelyben az eszköz konfigurációja érvényes.</span><span class="sxs-lookup"><span data-stu-id="7144a-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="7144a-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7144a-151">-Confirm</span></span>
<span data-ttu-id="7144a-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7144a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7144a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7144a-153">-WhatIf</span></span>
<span data-ttu-id="7144a-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7144a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7144a-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7144a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7144a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7144a-156">CommonParameters</span></span>
<span data-ttu-id="7144a-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7144a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7144a-158">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7144a-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7144a-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7144a-159">INPUTS</span></span>

### <span data-ttu-id="7144a-160">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7144a-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7144a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7144a-161">System.String</span></span>

## <span data-ttu-id="7144a-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7144a-162">OUTPUTS</span></span>

### <span data-ttu-id="7144a-163">Microsoft. Azure. Command. Management. IotHub. models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="7144a-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="7144a-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7144a-164">NOTES</span></span>

## <span data-ttu-id="7144a-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7144a-165">RELATED LINKS</span></span>
