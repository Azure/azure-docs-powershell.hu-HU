---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a7c99e2ce307d700e43094ffa9be47e5449acc0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411653"
---
# <span data-ttu-id="e70f4-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e70f4-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="e70f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e70f4-102">SYNOPSIS</span></span>
<span data-ttu-id="e70f4-103">A webhely-helyreállítási tároló műveleti adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e70f4-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="e70f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e70f4-104">SYNTAX</span></span>

### <span data-ttu-id="e70f4-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e70f4-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e70f4-106">ById</span><span class="sxs-lookup"><span data-stu-id="e70f4-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e70f4-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="e70f4-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e70f4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e70f4-108">DESCRIPTION</span></span>
<span data-ttu-id="e70f4-109">A **Get-AzureSiteRecoveryCm** parancsmag azure-webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="e70f4-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="e70f4-110">Ezzel a parancsmagkal megtekintheti az aktuális webhely-helyreállítási tároló műveleti adatait.</span><span class="sxs-lookup"><span data-stu-id="e70f4-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="e70f4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e70f4-111">EXAMPLES</span></span>

### <span data-ttu-id="e70f4-112">1. példa: Feladat lehozása azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="e70f4-112">Example 1: Get a job by specifying an ID</span></span>
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

<span data-ttu-id="e70f4-113">Ez a parancs lekérte az Azure-webhely-helyreállítási feladatot, amely a megadott azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="e70f4-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="e70f4-114">2. példa: Munkát kap az idő alapján</span><span class="sxs-lookup"><span data-stu-id="e70f4-114">Example 2: Gets a job based on time</span></span>
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

<span data-ttu-id="e70f4-115">Ez a parancs a megadott kezdési és záró időpont közé eső webhely-helyreállítási feladatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e70f4-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="e70f4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e70f4-116">PARAMETERS</span></span>

### <span data-ttu-id="e70f4-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e70f4-117">-EndTime</span></span>
<span data-ttu-id="e70f4-118">A feladatok záró idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70f4-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="e70f4-119">Ez a parancsmag az összes olyan munkát begyakorlja, amely a megadott időpont előtt kezdődött.</span><span class="sxs-lookup"><span data-stu-id="e70f4-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="e70f4-120">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e70f4-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e70f4-121">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e70f4-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="e70f4-122">-Id</span><span class="sxs-lookup"><span data-stu-id="e70f4-122">-Id</span></span>
<span data-ttu-id="e70f4-123">A be szereznie kell egy feladat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70f4-123">Specifies the ID of a job to get.</span></span>

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

### <span data-ttu-id="e70f4-124">-Job</span><span class="sxs-lookup"><span data-stu-id="e70f4-124">-Job</span></span>
<span data-ttu-id="e70f4-125">Meg kell kapnia egy feladatot.</span><span class="sxs-lookup"><span data-stu-id="e70f4-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="e70f4-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e70f4-126">-Profile</span></span>
<span data-ttu-id="e70f4-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="e70f4-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e70f4-128">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="e70f4-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e70f4-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e70f4-129">-StartTime</span></span>
<span data-ttu-id="e70f4-130">A feladatok kezdési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70f4-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="e70f4-131">Ez a parancsmag az összes olyan munkát begyakorlja, amely a megadott idő után kezdődött.</span><span class="sxs-lookup"><span data-stu-id="e70f4-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="e70f4-132">-State</span><span class="sxs-lookup"><span data-stu-id="e70f4-132">-State</span></span>
<span data-ttu-id="e70f4-133">A webhely-helyreállítási feladat bemeneti állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70f4-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="e70f4-134">Ez a parancsmag a megadott állapotnak megfelelő összes munkakört beveszi.</span><span class="sxs-lookup"><span data-stu-id="e70f4-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="e70f4-135">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="e70f4-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e70f4-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="e70f4-136">NotStarted</span></span>
- <span data-ttu-id="e70f4-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="e70f4-137">InProgress</span></span>
- <span data-ttu-id="e70f4-138">Sikeres</span><span class="sxs-lookup"><span data-stu-id="e70f4-138">Succeeded</span></span>
- <span data-ttu-id="e70f4-139">Egyéb</span><span class="sxs-lookup"><span data-stu-id="e70f4-139">Other</span></span>
- <span data-ttu-id="e70f4-140">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="e70f4-140">Failed</span></span>
- <span data-ttu-id="e70f4-141">Megszakítva</span><span class="sxs-lookup"><span data-stu-id="e70f4-141">Cancelled</span></span>
- <span data-ttu-id="e70f4-142">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="e70f4-142">Suspended</span></span>

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

### <span data-ttu-id="e70f4-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="e70f4-143">-TargetObjectId</span></span>
<span data-ttu-id="e70f4-144">A feladat által megcélzott objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e70f4-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="e70f4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70f4-145">CommonParameters</span></span>
<span data-ttu-id="e70f4-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e70f4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70f4-147">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e70f4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70f4-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e70f4-148">INPUTS</span></span>

## <span data-ttu-id="e70f4-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e70f4-149">OUTPUTS</span></span>

## <span data-ttu-id="e70f4-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e70f4-150">NOTES</span></span>

## <span data-ttu-id="e70f4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e70f4-151">RELATED LINKS</span></span>



[<span data-ttu-id="e70f4-152">Restart-AzureSiteRecoveryÚt</span><span class="sxs-lookup"><span data-stu-id="e70f4-152">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e70f4-153">Resume-AzureSiteRecoveryÚt</span><span class="sxs-lookup"><span data-stu-id="e70f4-153">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e70f4-154">Stop-AzureSiteRecoveryÚt</span><span class="sxs-lookup"><span data-stu-id="e70f4-154">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


