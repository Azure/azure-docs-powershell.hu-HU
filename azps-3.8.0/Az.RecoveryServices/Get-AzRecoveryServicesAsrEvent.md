---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846969"
---
# <span data-ttu-id="cc9ef-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="cc9ef-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="cc9ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9ef-103">Információt kap az Azure webhely-helyreállítási eseményekről a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="cc9ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc9ef-104">SYNTAX</span></span>

### <span data-ttu-id="cc9ef-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc9ef-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc9ef-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc9ef-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc9ef-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="cc9ef-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc9ef-108">ByName</span><span class="sxs-lookup"><span data-stu-id="cc9ef-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc9ef-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc9ef-109">DESCRIPTION</span></span>
<span data-ttu-id="cc9ef-110">A **Get-AzRecoveryServicesAsrEvent** a megadott kijelölési szűrők alapján kapja meg az események listáját a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="cc9ef-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cc9ef-111">EXAMPLES</span></span>

### <span data-ttu-id="cc9ef-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc9ef-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="cc9ef-113">Az összes esemény listája.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-113">List of all events.</span></span>

### <span data-ttu-id="cc9ef-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="cc9ef-114">Example 2</span></span>
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

<span data-ttu-id="cc9ef-115">Az esemény beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="cc9ef-115">Get event by name.</span></span>

### <span data-ttu-id="cc9ef-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="cc9ef-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="cc9ef-117">Az érintett objektum eseményének listája.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-117">List of event for affected Object.</span></span>

### <span data-ttu-id="cc9ef-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="cc9ef-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="cc9ef-119">Az események listája a kezdés időpontja és a Befejezés időpontja között, a kritikus és az egészség típusú VmHealth súlyossága.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="cc9ef-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-120">PARAMETERS</span></span>

### <span data-ttu-id="cc9ef-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cc9ef-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="cc9ef-122">A keresés AffectedObject típusú megjelenített adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-122">Specifies AffectedObject FriendlyName for the search.</span></span>

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

### <span data-ttu-id="cc9ef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9ef-123">-DefaultProfile</span></span>
<span data-ttu-id="cc9ef-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc9ef-125">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="cc9ef-125">-EndTime</span></span>
<span data-ttu-id="cc9ef-126">A keresési ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="cc9ef-127">Ezzel a paraméterrel csak azokat az eseményeket érheti el, amelyek a megadott időpontig bekövetkeztek.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

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

### <span data-ttu-id="cc9ef-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="cc9ef-128">-EventType</span></span>
<span data-ttu-id="cc9ef-129">Események szűrése az esemény típusával.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-129">Filter events by the event type.</span></span>

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

### <span data-ttu-id="cc9ef-130">-Szövet</span><span class="sxs-lookup"><span data-stu-id="cc9ef-130">-Fabric</span></span>
<span data-ttu-id="cc9ef-131">Az események szűrése a megadott anyag szerint</span><span class="sxs-lookup"><span data-stu-id="cc9ef-131">Filter events by the specified fabric.</span></span>

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

### <span data-ttu-id="cc9ef-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="cc9ef-132">-FabricId</span></span>
<span data-ttu-id="cc9ef-133">A szűrni kívánt fabricId adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-133">Specifies the fabricId to filter.</span></span>

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

### <span data-ttu-id="cc9ef-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc9ef-134">-Name</span></span>
<span data-ttu-id="cc9ef-135">A keresés eseményének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-135">Specifies name of the event for search.</span></span>

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

### <span data-ttu-id="cc9ef-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc9ef-136">-ResourceId</span></span>
<span data-ttu-id="cc9ef-137">Az esemény ResourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-137">Specifies the event ResourceId of event.</span></span>

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

### <span data-ttu-id="cc9ef-138">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="cc9ef-138">-Severity</span></span>
<span data-ttu-id="cc9ef-139">Esemény súlyossága a szűréshez.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-139">Event severity to filter on.</span></span>

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

### <span data-ttu-id="cc9ef-140">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="cc9ef-140">-StartTime</span></span>
<span data-ttu-id="cc9ef-141">A keresés ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="cc9ef-142">Ezzel a paraméterrel csak azokat az eseményeket érheti el, amelyek a megadott idő után léptek fel.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

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

### <span data-ttu-id="cc9ef-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9ef-143">CommonParameters</span></span>
<span data-ttu-id="cc9ef-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc9ef-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9ef-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc9ef-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9ef-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-146">INPUTS</span></span>

### <span data-ttu-id="cc9ef-147">System. String</span><span class="sxs-lookup"><span data-stu-id="cc9ef-147">System.String</span></span>

## <span data-ttu-id="cc9ef-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-148">OUTPUTS</span></span>

### <span data-ttu-id="cc9ef-149">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="cc9ef-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="cc9ef-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc9ef-150">NOTES</span></span>

## <span data-ttu-id="cc9ef-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc9ef-151">RELATED LINKS</span></span>