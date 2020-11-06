---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503988"
---
# <span data-ttu-id="79986-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79986-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="79986-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79986-102">SYNOPSIS</span></span>
<span data-ttu-id="79986-103">A megadott ASR-feladat részleteit vagy a legutóbbi ASR-feladatok listáját a helyreállítási szolgáltatások pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="79986-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79986-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79986-104">SYNTAX</span></span>

### <span data-ttu-id="79986-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79986-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="79986-106">ByName</span><span class="sxs-lookup"><span data-stu-id="79986-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="79986-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="79986-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="79986-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="79986-108">DESCRIPTION</span></span>
<span data-ttu-id="79986-109">A **Get-AzureRmRecoveryServicesAsrJob** parancsmag Azure webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="79986-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="79986-110">Ezzel a parancsmaggal megtekintheti az ASR-feladatokat a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="79986-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="79986-111">Példák</span><span class="sxs-lookup"><span data-stu-id="79986-111">EXAMPLES</span></span>

### <span data-ttu-id="79986-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="79986-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="79986-113">Egy adott ASR-objektum összes feladatát visszaadja (az ASR-objektumra (például a többszörözött elemre vagy a helyreállítási csomagra) az AZONOSÍTÓval.)</span><span class="sxs-lookup"><span data-stu-id="79986-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="79986-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79986-114">PARAMETERS</span></span>

### <span data-ttu-id="79986-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="79986-115">-EndTime</span></span>
<span data-ttu-id="79986-116">A feladatok befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="79986-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="79986-117">Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="79986-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="79986-118">Ha egy **datetime** objektumot szeretne beolvasni ehhez a paraméterhez, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="79986-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="79986-119">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="79986-119">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="79986-120">-Job</span><span class="sxs-lookup"><span data-stu-id="79986-120">-Job</span></span>
<span data-ttu-id="79986-121">Az ASR-feladat objektumát adja meg, amely frissíti a részleteket.</span><span class="sxs-lookup"><span data-stu-id="79986-121">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="79986-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79986-122">-Name</span></span>
<span data-ttu-id="79986-123">Adja meg az ASR-feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="79986-123">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="79986-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="79986-124">-StartTime</span></span>
<span data-ttu-id="79986-125">A feladatok kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="79986-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="79986-126">Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.</span><span class="sxs-lookup"><span data-stu-id="79986-126">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="79986-127">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="79986-127">-State</span></span>
<span data-ttu-id="79986-128">Az ASR-feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="79986-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="79986-129">Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="79986-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="79986-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="79986-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79986-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="79986-131">NotStarted</span></span>
- <span data-ttu-id="79986-132">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="79986-132">InProgress</span></span>
- <span data-ttu-id="79986-133">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="79986-133">Succeeded</span></span>
- <span data-ttu-id="79986-134">Más</span><span class="sxs-lookup"><span data-stu-id="79986-134">Other</span></span>
- <span data-ttu-id="79986-135">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="79986-135">Failed</span></span>
- <span data-ttu-id="79986-136">Lemondott</span><span class="sxs-lookup"><span data-stu-id="79986-136">Cancelled</span></span>
- <span data-ttu-id="79986-137">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="79986-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79986-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="79986-138">-TargetObjectId</span></span>
<span data-ttu-id="79986-139">Az objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="79986-139">Specifies the ID of the object.</span></span> <span data-ttu-id="79986-140">A megadott objektumon a feladatok keresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="79986-140">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="79986-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79986-141">CommonParameters</span></span>
<span data-ttu-id="79986-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79986-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79986-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79986-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79986-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79986-144">INPUTS</span></span>

### <span data-ttu-id="79986-145">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="79986-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79986-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79986-146">OUTPUTS</span></span>

### <span data-ttu-id="79986-147">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="79986-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="79986-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79986-148">NOTES</span></span>

## <span data-ttu-id="79986-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79986-149">RELATED LINKS</span></span>

[<span data-ttu-id="79986-150">Újraindítás – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79986-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="79986-151">Önéletrajz – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79986-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="79986-152">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79986-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
