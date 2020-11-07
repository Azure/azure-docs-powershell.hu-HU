---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a24b5e5d4cce1e33536b7977590add11a6d7cb39
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844073"
---
# <span data-ttu-id="00b7d-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="00b7d-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="00b7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="00b7d-103">Az eszközön található triggert adja meg.</span><span class="sxs-lookup"><span data-stu-id="00b7d-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="00b7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00b7d-104">SYNTAX</span></span>

### <span data-ttu-id="00b7d-105">FileEventTriggerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00b7d-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00b7d-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="00b7d-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00b7d-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00b7d-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00b7d-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00b7d-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00b7d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="00b7d-109">DESCRIPTION</span></span>
<span data-ttu-id="00b7d-110">A **New-AzDataBoxEdgeTrigger** parancsmag az adatmező szélén lévő eszközön állítja be az aktiválást.</span><span class="sxs-lookup"><span data-stu-id="00b7d-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="00b7d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="00b7d-111">EXAMPLES</span></span>

### <span data-ttu-id="00b7d-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00b7d-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="00b7d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00b7d-113">PARAMETERS</span></span>

### <span data-ttu-id="00b7d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00b7d-114">-AsJob</span></span>
<span data-ttu-id="00b7d-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="00b7d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00b7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b7d-116">-DefaultProfile</span></span>
<span data-ttu-id="00b7d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00b7d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00b7d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="00b7d-118">-DeviceName</span></span>
<span data-ttu-id="00b7d-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="00b7d-119">Device Name</span></span>

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

### <span data-ttu-id="00b7d-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="00b7d-120">-FileEvent</span></span>
<span data-ttu-id="00b7d-121">Adja át ezt a kapcsoló paramétert a FileEvent-trigger beállításához</span><span class="sxs-lookup"><span data-stu-id="00b7d-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="00b7d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="00b7d-122">-Name</span></span>
<span data-ttu-id="00b7d-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="00b7d-123">Resource Name</span></span>

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

### <span data-ttu-id="00b7d-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="00b7d-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="00b7d-125">Adja át ezt a kapcsoló paramétert a PeriodicTimerEvent-trigger beállításához</span><span class="sxs-lookup"><span data-stu-id="00b7d-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="00b7d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b7d-126">-ResourceGroupName</span></span>
<span data-ttu-id="00b7d-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="00b7d-127">Resource Group Name</span></span>

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

### <span data-ttu-id="00b7d-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="00b7d-128">-RoleName</span></span>
<span data-ttu-id="00b7d-129">Kiszámítja, hogy mely eseményeket fogja növelni a program.</span><span class="sxs-lookup"><span data-stu-id="00b7d-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="00b7d-130">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="00b7d-130">-Schedule</span></span>
<span data-ttu-id="00b7d-131">Az az időszakos gyakoriság, amelyen az időzítő eseményt emelni kell.</span><span class="sxs-lookup"><span data-stu-id="00b7d-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="00b7d-132">Adja meg az ütemtervet (1 és 365 között), az órákat (1 és 23 között) vagy percekben (1 és 59 között).</span><span class="sxs-lookup"><span data-stu-id="00b7d-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="00b7d-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="00b7d-133">-ShareId</span></span>
<span data-ttu-id="00b7d-134">A FileEvent-triggerben átadott fájlmegosztás-azonosító</span><span class="sxs-lookup"><span data-stu-id="00b7d-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="00b7d-135">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="00b7d-135">-ShareName</span></span>
<span data-ttu-id="00b7d-136">A FileEvent-triggerben átadott fájlmegosztás-azonosító</span><span class="sxs-lookup"><span data-stu-id="00b7d-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="00b7d-137">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="00b7d-137">-StartTime</span></span>
<span data-ttu-id="00b7d-138">Az érvényes triggert eredményező nap időpontja.</span><span class="sxs-lookup"><span data-stu-id="00b7d-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="00b7d-139">A program az ütemezést a másodpercben megadott időpontra mutató hivatkozással számítja ki.</span><span class="sxs-lookup"><span data-stu-id="00b7d-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="00b7d-140">Ha az időzóna nincs megadva, az idő az eszköz időzónájában fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="00b7d-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="00b7d-141">Az érték mindig az UTC-időpontként fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="00b7d-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="00b7d-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="00b7d-142">-Topic</span></span>
<span data-ttu-id="00b7d-143">A IoT-eszközön ismétlődő eseményeket közzétevő téma</span><span class="sxs-lookup"><span data-stu-id="00b7d-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="00b7d-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00b7d-144">-Confirm</span></span>
<span data-ttu-id="00b7d-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00b7d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00b7d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00b7d-146">-WhatIf</span></span>
<span data-ttu-id="00b7d-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00b7d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00b7d-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00b7d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00b7d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b7d-149">CommonParameters</span></span>
<span data-ttu-id="00b7d-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00b7d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b7d-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="00b7d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b7d-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00b7d-152">INPUTS</span></span>

### <span data-ttu-id="00b7d-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="00b7d-153">None</span></span>

## <span data-ttu-id="00b7d-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00b7d-154">OUTPUTS</span></span>

### <span data-ttu-id="00b7d-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="00b7d-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="00b7d-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00b7d-156">NOTES</span></span>

## <span data-ttu-id="00b7d-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00b7d-157">RELATED LINKS</span></span>
