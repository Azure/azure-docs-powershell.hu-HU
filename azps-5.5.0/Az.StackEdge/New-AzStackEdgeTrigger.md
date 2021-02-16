---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155091"
---
# <span data-ttu-id="9fe4d-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="9fe4d-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="9fe4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fe4d-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe4d-103">Konfigurál egy eseményindítót az eszközön.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="9fe4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9fe4d-104">SYNTAX</span></span>

### <span data-ttu-id="9fe4d-105">FileEventTriggerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fe4d-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe4d-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe4d-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe4d-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe4d-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe4d-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe4d-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe4d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9fe4d-109">DESCRIPTION</span></span>
<span data-ttu-id="9fe4d-110">A **New-AzStackEdgeTrigger** parancsmag konfigurál egy eseményindítót a Stack Edge eszközön.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="9fe4d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9fe4d-111">EXAMPLES</span></span>

### <span data-ttu-id="9fe4d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9fe4d-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="9fe4d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fe4d-113">PARAMETERS</span></span>

### <span data-ttu-id="9fe4d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fe4d-114">-AsJob</span></span>
<span data-ttu-id="9fe4d-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9fe4d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fe4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe4d-116">-DefaultProfile</span></span>
<span data-ttu-id="9fe4d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe4d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9fe4d-118">-DeviceName</span></span>
<span data-ttu-id="9fe4d-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="9fe4d-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4d-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="9fe4d-120">-FileEvent</span></span>
<span data-ttu-id="9fe4d-121">Adja át ezt a kapcsoló paramétert a FileEvent trigger konfigurálása</span><span class="sxs-lookup"><span data-stu-id="9fe4d-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="9fe4d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9fe4d-122">-Name</span></span>
<span data-ttu-id="9fe4d-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9fe4d-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4d-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="9fe4d-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="9fe4d-125">Adja át ezt a kapcsoló paramétert a PeriodicTimerEvent trigger konfigurálása</span><span class="sxs-lookup"><span data-stu-id="9fe4d-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="9fe4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9fe4d-127">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9fe4d-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4d-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="9fe4d-128">-RoleName</span></span>
<span data-ttu-id="9fe4d-129">Annak a szerepkörnek a kiszámítása, amellyel össze szeretné számítani az eseményeket.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="9fe4d-130">-Schedule</span><span class="sxs-lookup"><span data-stu-id="9fe4d-130">-Schedule</span></span>
<span data-ttu-id="9fe4d-131">Periodikus gyakoriság, amikorra fel kell emelni az időzítőeseményt.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="9fe4d-132">Adjon meg egy ütemezést mindkét napon (1 és 365 között), órákban (1 és 23 között), illetve percben (1 és 59 között).</span><span class="sxs-lookup"><span data-stu-id="9fe4d-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="9fe4d-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="9fe4d-133">-ShareId</span></span>
<span data-ttu-id="9fe4d-134">A FileEvent Triggerben átadott fájlmegosztási azonosító</span><span class="sxs-lookup"><span data-stu-id="9fe4d-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="9fe4d-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9fe4d-135">-ShareName</span></span>
<span data-ttu-id="9fe4d-136">A FileEvent Triggerben átadott fájlmegosztási azonosító</span><span class="sxs-lookup"><span data-stu-id="9fe4d-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="9fe4d-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9fe4d-137">-StartTime</span></span>
<span data-ttu-id="9fe4d-138">A nap érvényes eseményindítót ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="9fe4d-139">Az ütemezés kiszámítása legfeljebb másodpercben megadott időpontra való hivatkozással történt.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="9fe4d-140">Ha az időzóna nincs megadva, akkor az idő az eszköz időzónában valónak minősül.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="9fe4d-141">Az érték mindig UTC-időként lesz visszaadva.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="9fe4d-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="9fe4d-142">-Topic</span></span>
<span data-ttu-id="9fe4d-143">Az IoT-eszközön rendszeres eseményeket közzétenő témakör.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="9fe4d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fe4d-144">-Confirm</span></span>
<span data-ttu-id="9fe4d-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe4d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe4d-146">-WhatIf</span></span>
<span data-ttu-id="9fe4d-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fe4d-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe4d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe4d-149">CommonParameters</span></span>
<span data-ttu-id="9fe4d-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe4d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe4d-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fe4d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe4d-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fe4d-152">INPUTS</span></span>

### <span data-ttu-id="9fe4d-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="9fe4d-153">None</span></span>

## <span data-ttu-id="9fe4d-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fe4d-154">OUTPUTS</span></span>

### <span data-ttu-id="9fe4d-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="9fe4d-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="9fe4d-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9fe4d-156">NOTES</span></span>

## <span data-ttu-id="9fe4d-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fe4d-157">RELATED LINKS</span></span>
