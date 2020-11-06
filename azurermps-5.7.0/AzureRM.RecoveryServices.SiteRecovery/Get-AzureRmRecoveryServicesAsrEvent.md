---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500452"
---
# <span data-ttu-id="6b377-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="6b377-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="6b377-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b377-102">SYNOPSIS</span></span>
<span data-ttu-id="6b377-103">Információt kap az Azure webhely-helyreállítási eseményekről a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="6b377-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b377-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b377-104">SYNTAX</span></span>

### <span data-ttu-id="6b377-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b377-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b377-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b377-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b377-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="6b377-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b377-108">ByName</span><span class="sxs-lookup"><span data-stu-id="6b377-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b377-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b377-109">DESCRIPTION</span></span>
<span data-ttu-id="6b377-110">A **Get-AzureRmRecoveryServicesAsrEvent** a megadott kijelölési szűrők alapján kapja meg az események listáját a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="6b377-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="6b377-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6b377-111">EXAMPLES</span></span>

### <span data-ttu-id="6b377-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6b377-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="6b377-113">Az összes esemény listája.</span><span class="sxs-lookup"><span data-stu-id="6b377-113">List of all events.</span></span>

### <span data-ttu-id="6b377-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="6b377-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="6b377-115">Az esemény beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="6b377-115">Get event by name.</span></span>

### <span data-ttu-id="6b377-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="6b377-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="6b377-117">Az érintett objektum eseményének listája.</span><span class="sxs-lookup"><span data-stu-id="6b377-117">List of event for affected Object.</span></span>

### <span data-ttu-id="6b377-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="6b377-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="6b377-119">Az események listája a kezdés időpontja és a Befejezés időpontja között, a kritikus és az egészség típusú VmHealth súlyossága.</span><span class="sxs-lookup"><span data-stu-id="6b377-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="6b377-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b377-120">PARAMETERS</span></span>

### <span data-ttu-id="6b377-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b377-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="6b377-122">A keresés AffectedObject típusú megjelenített adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b377-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b377-123">-DefaultProfile</span></span>
<span data-ttu-id="6b377-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b377-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-125">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="6b377-125">-EndTime</span></span>
<span data-ttu-id="6b377-126">A keresési ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b377-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="6b377-127">Ezzel a paraméterrel csak azokat az eseményeket érheti el, amelyek a megadott időpontig bekövetkeztek.</span><span class="sxs-lookup"><span data-stu-id="6b377-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="6b377-128">-EventType</span></span>
<span data-ttu-id="6b377-129">Események szűrése az esemény típusával.</span><span class="sxs-lookup"><span data-stu-id="6b377-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-130">-Szövet</span><span class="sxs-lookup"><span data-stu-id="6b377-130">-Fabric</span></span>
<span data-ttu-id="6b377-131">Az események szűrése a megadott anyag szerint</span><span class="sxs-lookup"><span data-stu-id="6b377-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="6b377-132">-FabricId</span></span>
<span data-ttu-id="6b377-133">A szűrni kívánt fabricId adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b377-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b377-134">-Name</span></span>
<span data-ttu-id="6b377-135">A keresés eseményének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b377-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b377-136">-ResourceId</span></span>
<span data-ttu-id="6b377-137">Specifes az esemény ReourceId.</span><span class="sxs-lookup"><span data-stu-id="6b377-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-138">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="6b377-138">-Severity</span></span>
<span data-ttu-id="6b377-139">Esemény súlyossága a szűréshez.</span><span class="sxs-lookup"><span data-stu-id="6b377-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-140">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="6b377-140">-StartTime</span></span>
<span data-ttu-id="6b377-141">A keresés ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b377-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="6b377-142">Ezzel a paraméterrel csak azokat az eseményeket érheti el, amelyek a megadott idő után léptek fel.</span><span class="sxs-lookup"><span data-stu-id="6b377-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b377-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b377-143">CommonParameters</span></span>
<span data-ttu-id="6b377-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b377-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b377-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b377-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b377-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b377-146">INPUTS</span></span>

### <span data-ttu-id="6b377-147">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6b377-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6b377-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b377-148">OUTPUTS</span></span>

### <span data-ttu-id="6b377-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASREvent, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6b377-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6b377-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b377-150">NOTES</span></span>

## <span data-ttu-id="6b377-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b377-151">RELATED LINKS</span></span>
