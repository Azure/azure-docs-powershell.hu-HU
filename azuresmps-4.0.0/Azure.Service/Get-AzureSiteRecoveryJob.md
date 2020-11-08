---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015595"
---
# <span data-ttu-id="d7e6a-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d7e6a-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="d7e6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e6a-103">A webhely-helyreállítási boltozat üzemeltetési adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="d7e6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7e6a-104">SYNTAX</span></span>

### <span data-ttu-id="d7e6a-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7e6a-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d7e6a-106">ById</span><span class="sxs-lookup"><span data-stu-id="d7e6a-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d7e6a-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="d7e6a-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d7e6a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7e6a-108">DESCRIPTION</span></span>
<span data-ttu-id="d7e6a-109">A **Get-AzureSiteRecoveryJob** parancsmag Azure webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="d7e6a-110">Ezzel a parancsmaggal megtekintheti az aktuális webhely-helyreállítási boltozat üzemeltetési adatait.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="d7e6a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d7e6a-111">EXAMPLES</span></span>

### <span data-ttu-id="d7e6a-112">Példa 1: egy azonosító megadásával munka beszerzése</span><span class="sxs-lookup"><span data-stu-id="d7e6a-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="d7e6a-113">Ez a parancs a megadott AZONOSÍTÓJÚ Azure webhely-helyreállítási feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="d7e6a-114">2. példa: a munka időben alapul</span><span class="sxs-lookup"><span data-stu-id="d7e6a-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="d7e6a-115">Ez a parancs a megadott kezdési és befejezési időpontot tartalmazó webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="d7e6a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7e6a-116">PARAMETERS</span></span>

### <span data-ttu-id="d7e6a-117">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="d7e6a-117">-EndTime</span></span>
<span data-ttu-id="d7e6a-118">A feladatok befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="d7e6a-119">Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="d7e6a-120">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="d7e6a-121">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d7e6a-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e6a-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d7e6a-122">-Id</span></span>
<span data-ttu-id="d7e6a-123">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e6a-124">-Job</span><span class="sxs-lookup"><span data-stu-id="d7e6a-124">-Job</span></span>
<span data-ttu-id="d7e6a-125">A beolvasott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-125">Specifies a job to get.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e6a-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="d7e6a-126">-Profile</span></span>
<span data-ttu-id="d7e6a-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7e6a-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e6a-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="d7e6a-129">-StartTime</span></span>
<span data-ttu-id="d7e6a-130">A feladatok kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="d7e6a-131">Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-131">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e6a-132">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="d7e6a-132">-State</span></span>
<span data-ttu-id="d7e6a-133">A webhely-helyreállítási feladatok beviteli állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="d7e6a-134">Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="d7e6a-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7e6a-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7e6a-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="d7e6a-136">NotStarted</span></span>
- <span data-ttu-id="d7e6a-137">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="d7e6a-137">InProgress</span></span>
- <span data-ttu-id="d7e6a-138">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="d7e6a-138">Succeeded</span></span>
- <span data-ttu-id="d7e6a-139">Más</span><span class="sxs-lookup"><span data-stu-id="d7e6a-139">Other</span></span>
- <span data-ttu-id="d7e6a-140">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="d7e6a-140">Failed</span></span>
- <span data-ttu-id="d7e6a-141">Lemondott</span><span class="sxs-lookup"><span data-stu-id="d7e6a-141">Cancelled</span></span>
- <span data-ttu-id="d7e6a-142">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="d7e6a-142">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e6a-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="d7e6a-143">-TargetObjectId</span></span>
<span data-ttu-id="d7e6a-144">A feladat által célzott objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6a-144">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e6a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e6a-145">CommonParameters</span></span>
<span data-ttu-id="d7e6a-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7e6a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e6a-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e6a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e6a-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e6a-148">INPUTS</span></span>

## <span data-ttu-id="d7e6a-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e6a-149">OUTPUTS</span></span>

## <span data-ttu-id="d7e6a-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7e6a-150">NOTES</span></span>

## <span data-ttu-id="d7e6a-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7e6a-151">RELATED LINKS</span></span>

[<span data-ttu-id="d7e6a-152">Azure site Recovery Services-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d7e6a-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="d7e6a-153">Újraindítás – AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d7e6a-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d7e6a-154">Önéletrajz – AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d7e6a-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d7e6a-155">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d7e6a-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


