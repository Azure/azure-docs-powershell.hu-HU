---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 52c694010673d11c269f94a05474e9399e87c962
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941450"
---
# <span data-ttu-id="a94de-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="a94de-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="a94de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a94de-102">SYNOPSIS</span></span>
<span data-ttu-id="a94de-103">Az Azure-webhely-helyreállítási események részletei a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a94de-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="a94de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a94de-104">SYNTAX</span></span>

### <span data-ttu-id="a94de-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a94de-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a94de-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a94de-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a94de-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="a94de-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a94de-108">ByName</span><span class="sxs-lookup"><span data-stu-id="a94de-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a94de-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a94de-109">DESCRIPTION</span></span>
<span data-ttu-id="a94de-110">A **Get-AzRecoveryServicesAsrEvent** a megadott kijelölési szűrők alapján megkapja a tárolóban található események listáját.</span><span class="sxs-lookup"><span data-stu-id="a94de-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="a94de-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a94de-111">EXAMPLES</span></span>

### <span data-ttu-id="a94de-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a94de-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="a94de-113">Az összes esemény listája.</span><span class="sxs-lookup"><span data-stu-id="a94de-113">List of all events.</span></span>

### <span data-ttu-id="a94de-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a94de-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="a94de-115">Esemény lekérte név szerint.</span><span class="sxs-lookup"><span data-stu-id="a94de-115">Get event by name.</span></span>

### <span data-ttu-id="a94de-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a94de-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="a94de-117">Az érintett objektum eseményének listája.</span><span class="sxs-lookup"><span data-stu-id="a94de-117">List of event for affected Object.</span></span>

### <span data-ttu-id="a94de-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="a94de-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="a94de-119">Az esemény listája a kezdési és a záró időpont, a súlyosság kritikus és az állapot típusa VmHealth között.</span><span class="sxs-lookup"><span data-stu-id="a94de-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="a94de-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a94de-120">PARAMETERS</span></span>

### <span data-ttu-id="a94de-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a94de-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="a94de-122">Az AffectedObject FriendlyName paramétert adja meg a kereséshez.</span><span class="sxs-lookup"><span data-stu-id="a94de-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94de-123">-DefaultProfile</span></span>
<span data-ttu-id="a94de-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a94de-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a94de-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a94de-125">-EndTime</span></span>
<span data-ttu-id="a94de-126">A keresési ablak záró idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a94de-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="a94de-127">Ezzel a paraméterrel csak azokat az eseményeket szerezze be, amelyek a megadott időpont előtt történtek.</span><span class="sxs-lookup"><span data-stu-id="a94de-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="a94de-128">-EventType</span></span>
<span data-ttu-id="a94de-129">Események szűrése az esemény típusa szerint.</span><span class="sxs-lookup"><span data-stu-id="a94de-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="a94de-130">-Fabric</span></span>
<span data-ttu-id="a94de-131">Az eseményeket a megadott anyag szerint szűrheti.</span><span class="sxs-lookup"><span data-stu-id="a94de-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="a94de-132">-FabricId</span></span>
<span data-ttu-id="a94de-133">Megadja a szűréshez a fabricId tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="a94de-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a94de-134">-Name</span></span>
<span data-ttu-id="a94de-135">A kereséshez megadott esemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a94de-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a94de-136">-ResourceId</span></span>
<span data-ttu-id="a94de-137">Az esemény erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a94de-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-138">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="a94de-138">-Severity</span></span>
<span data-ttu-id="a94de-139">Az esemény súlyossága, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="a94de-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a94de-140">-StartTime</span></span>
<span data-ttu-id="a94de-141">A keresési ablak kezdő idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a94de-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="a94de-142">Ezzel a paraméterrel csak azokat az eseményeket szerezze be, amelyek a megadott idő után történtek.</span><span class="sxs-lookup"><span data-stu-id="a94de-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94de-143">CommonParameters</span></span>
<span data-ttu-id="a94de-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94de-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a94de-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94de-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a94de-146">INPUTS</span></span>

### <span data-ttu-id="a94de-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a94de-147">System.String</span></span>

## <span data-ttu-id="a94de-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a94de-148">OUTPUTS</span></span>

### <span data-ttu-id="a94de-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span><span class="sxs-lookup"><span data-stu-id="a94de-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="a94de-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a94de-150">NOTES</span></span>

## <span data-ttu-id="a94de-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a94de-151">RELATED LINKS</span></span>
