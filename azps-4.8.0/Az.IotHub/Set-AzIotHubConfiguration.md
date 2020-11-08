---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181746"
---
# <span data-ttu-id="6968c-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="6968c-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="6968c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6968c-102">SYNOPSIS</span></span>
<span data-ttu-id="6968c-103">Frissítse a konfigurációs regisztráció változékony mezőit.</span><span class="sxs-lookup"><span data-stu-id="6968c-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="6968c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6968c-104">SYNTAX</span></span>

### <span data-ttu-id="6968c-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6968c-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6968c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6968c-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6968c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6968c-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6968c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6968c-108">DESCRIPTION</span></span>
<span data-ttu-id="6968c-109">A IoT automatikus eszközkezelés konfigurációjának meghatározott tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="6968c-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="6968c-110">Megjegyzés: a konfigurációs tartalmak nem állandók.</span><span class="sxs-lookup"><span data-stu-id="6968c-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="6968c-111">A frissíthető konfigurációs tulajdonságok "címkék", "metrikák", "prioritás" és "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="6968c-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="6968c-112"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="6968c-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="6968c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6968c-113">EXAMPLES</span></span>

### <span data-ttu-id="6968c-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6968c-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="6968c-115">Az eszközbeállítások prioritásának módosítása és a TARGET-feltétel frissítése</span><span class="sxs-lookup"><span data-stu-id="6968c-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="6968c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6968c-116">PARAMETERS</span></span>

### <span data-ttu-id="6968c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6968c-117">-DefaultProfile</span></span>
<span data-ttu-id="6968c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6968c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6968c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6968c-119">-Force</span></span>
<span data-ttu-id="6968c-120">Lehetővé teszi a konfigurációs objektum lecserélését abban az esetben is, ha a legutóbbi időponttól kezdve frissült.</span><span class="sxs-lookup"><span data-stu-id="6968c-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="6968c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6968c-121">-InputObject</span></span>
<span data-ttu-id="6968c-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="6968c-122">IotHub object</span></span>

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

### <span data-ttu-id="6968c-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6968c-123">-IotHubName</span></span>
<span data-ttu-id="6968c-124">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="6968c-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6968c-125">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="6968c-125">-Label</span></span>
<span data-ttu-id="6968c-126">A cél-konfigurációra alkalmazandó címkék megfeleltetése.</span><span class="sxs-lookup"><span data-stu-id="6968c-126">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="6968c-127">-Metrikus</span><span class="sxs-lookup"><span data-stu-id="6968c-127">-Metric</span></span>
<span data-ttu-id="6968c-128">Lekérdezések gyűjteménye a konfigurációs metrikák definícióhoz.</span><span class="sxs-lookup"><span data-stu-id="6968c-128">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="6968c-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6968c-129">-Name</span></span>
<span data-ttu-id="6968c-130">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6968c-130">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6968c-131">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="6968c-131">-Priority</span></span>
<span data-ttu-id="6968c-132">Az eszköz konfigurációjának súlya a versengő szabályok (legmagasabb WINS) esetén.</span><span class="sxs-lookup"><span data-stu-id="6968c-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="6968c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6968c-133">-ResourceGroupName</span></span>
<span data-ttu-id="6968c-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6968c-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6968c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6968c-135">-ResourceId</span></span>
<span data-ttu-id="6968c-136">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="6968c-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6968c-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="6968c-137">-TargetCondition</span></span>
<span data-ttu-id="6968c-138">Az a cél feltétel, amelyben az eszköz konfigurációja érvényes.</span><span class="sxs-lookup"><span data-stu-id="6968c-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="6968c-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6968c-139">-Confirm</span></span>
<span data-ttu-id="6968c-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6968c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6968c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6968c-141">-WhatIf</span></span>
<span data-ttu-id="6968c-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6968c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6968c-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6968c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6968c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6968c-144">CommonParameters</span></span>
<span data-ttu-id="6968c-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6968c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6968c-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6968c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6968c-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6968c-147">INPUTS</span></span>

### <span data-ttu-id="6968c-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6968c-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6968c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6968c-149">System.String</span></span>

## <span data-ttu-id="6968c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6968c-150">OUTPUTS</span></span>

### <span data-ttu-id="6968c-151">Microsoft. Azure. Command. Management. IotHub. models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="6968c-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="6968c-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6968c-152">NOTES</span></span>

## <span data-ttu-id="6968c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6968c-153">RELATED LINKS</span></span>
