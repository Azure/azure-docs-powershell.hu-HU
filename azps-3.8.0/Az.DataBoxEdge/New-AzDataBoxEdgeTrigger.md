---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: ac7fb7d6af2e04387ea4abfa3fe62c4df9271b13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012811"
---
# <span data-ttu-id="dd4a0-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="dd4a0-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="dd4a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4a0-103">Az eszközön található triggert adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="dd4a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd4a0-104">SYNTAX</span></span>

### <span data-ttu-id="dd4a0-105">FileEventTriggerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd4a0-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4a0-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd4a0-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4a0-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd4a0-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4a0-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd4a0-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd4a0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd4a0-109">DESCRIPTION</span></span>
<span data-ttu-id="dd4a0-110">A **New-AzDataBoxEdgeTrigger** parancsmag az adatmező szélén lévő eszközön állítja be az aktiválást.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="dd4a0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dd4a0-111">EXAMPLES</span></span>

### <span data-ttu-id="dd4a0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd4a0-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="dd4a0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd4a0-113">PARAMETERS</span></span>

### <span data-ttu-id="dd4a0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd4a0-114">-AsJob</span></span>
<span data-ttu-id="dd4a0-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dd4a0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd4a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4a0-116">-DefaultProfile</span></span>
<span data-ttu-id="dd4a0-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd4a0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dd4a0-118">-DeviceName</span></span>
<span data-ttu-id="dd4a0-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="dd4a0-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="dd4a0-120">-FileEvent</span></span>
<span data-ttu-id="dd4a0-121">Adja át ezt a kapcsoló paramétert a FileEvent-trigger beállításához</span><span class="sxs-lookup"><span data-stu-id="dd4a0-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd4a0-122">-Name</span></span>
<span data-ttu-id="dd4a0-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="dd4a0-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="dd4a0-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="dd4a0-125">Adja át ezt a kapcsoló paramétert a PeriodicTimerEvent-trigger beállításához</span><span class="sxs-lookup"><span data-stu-id="dd4a0-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd4a0-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="dd4a0-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="dd4a0-128">-RoleName</span></span>
<span data-ttu-id="dd4a0-129">Kiszámítja, hogy mely eseményeket fogja növelni a program.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-130">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="dd4a0-130">-Schedule</span></span>
<span data-ttu-id="dd4a0-131">Az az időszakos gyakoriság, amelyen az időzítő eseményt emelni kell.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="dd4a0-132">Adja meg az ütemtervet (1 és 365 között), az órákat (1 és 23 között) vagy percekben (1 és 59 között).</span><span class="sxs-lookup"><span data-stu-id="dd4a0-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="dd4a0-133">-ShareId</span></span>
<span data-ttu-id="dd4a0-134">A FileEvent-triggerben átadott fájlmegosztás-azonosító</span><span class="sxs-lookup"><span data-stu-id="dd4a0-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-135">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="dd4a0-135">-ShareName</span></span>
<span data-ttu-id="dd4a0-136">A FileEvent-triggerben átadott fájlmegosztás-azonosító</span><span class="sxs-lookup"><span data-stu-id="dd4a0-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-137">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="dd4a0-137">-StartTime</span></span>
<span data-ttu-id="dd4a0-138">Az érvényes triggert eredményező nap időpontja.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="dd4a0-139">A program az ütemezést a másodpercben megadott időpontra mutató hivatkozással számítja ki.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="dd4a0-140">Ha az időzóna nincs megadva, az idő az eszköz időzónájában fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="dd4a0-141">Az érték mindig az UTC-időpontként fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="dd4a0-142">-Topic</span></span>
<span data-ttu-id="dd4a0-143">A IoT-eszközön ismétlődő eseményeket közzétevő téma</span><span class="sxs-lookup"><span data-stu-id="dd4a0-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a0-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd4a0-144">-Confirm</span></span>
<span data-ttu-id="dd4a0-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd4a0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4a0-146">-WhatIf</span></span>
<span data-ttu-id="dd4a0-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd4a0-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd4a0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4a0-149">CommonParameters</span></span>
<span data-ttu-id="dd4a0-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd4a0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4a0-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4a0-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd4a0-152">INPUTS</span></span>

### <span data-ttu-id="dd4a0-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="dd4a0-153">None</span></span>

## <span data-ttu-id="dd4a0-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd4a0-154">OUTPUTS</span></span>

### <span data-ttu-id="dd4a0-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="dd4a0-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="dd4a0-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd4a0-156">NOTES</span></span>

## <span data-ttu-id="dd4a0-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd4a0-157">RELATED LINKS</span></span>
