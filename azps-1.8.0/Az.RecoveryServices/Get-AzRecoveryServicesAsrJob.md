---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669743"
---
# <span data-ttu-id="0c609-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0c609-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="0c609-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c609-102">SYNOPSIS</span></span>
<span data-ttu-id="0c609-103">A megadott ASR-feladat részleteit vagy a legutóbbi ASR-feladatok listáját a helyreállítási szolgáltatások pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="0c609-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="0c609-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c609-104">SYNTAX</span></span>

### <span data-ttu-id="0c609-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c609-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c609-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0c609-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c609-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="0c609-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c609-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c609-108">DESCRIPTION</span></span>
<span data-ttu-id="0c609-109">A **Get-AzRecoveryServicesAsrJob** parancsmag Azure webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="0c609-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="0c609-110">Ezzel a parancsmaggal megtekintheti az ASR-feladatokat a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="0c609-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="0c609-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0c609-111">EXAMPLES</span></span>

### <span data-ttu-id="0c609-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0c609-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="0c609-113">Egy adott ASR-objektum összes feladatát visszaadja (az ASR-objektumra (például a többszörözött elemre vagy a helyreállítási csomagra) az AZONOSÍTÓval.)</span><span class="sxs-lookup"><span data-stu-id="0c609-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="0c609-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c609-114">PARAMETERS</span></span>

### <span data-ttu-id="0c609-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c609-115">-DefaultProfile</span></span>
<span data-ttu-id="0c609-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c609-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0c609-117">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="0c609-117">-EndTime</span></span>
<span data-ttu-id="0c609-118">A feladatok befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c609-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="0c609-119">Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="0c609-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="0c609-120">Ha egy **datetime** objektumot szeretne beolvasni ehhez a paraméterhez, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0c609-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="0c609-121">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0c609-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c609-122">-Job</span><span class="sxs-lookup"><span data-stu-id="0c609-122">-Job</span></span>
<span data-ttu-id="0c609-123">Az ASR-feladat objektumát adja meg, amely frissíti a részleteket.</span><span class="sxs-lookup"><span data-stu-id="0c609-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c609-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c609-124">-Name</span></span>
<span data-ttu-id="0c609-125">Adja meg az ASR-feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="0c609-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="0c609-126">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="0c609-126">-StartTime</span></span>
<span data-ttu-id="0c609-127">A feladatok kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c609-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="0c609-128">Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.</span><span class="sxs-lookup"><span data-stu-id="0c609-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c609-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="0c609-129">-State</span></span>
<span data-ttu-id="0c609-130">Az ASR-feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c609-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="0c609-131">Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="0c609-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="0c609-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0c609-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c609-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="0c609-133">NotStarted</span></span>
- <span data-ttu-id="0c609-134">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="0c609-134">InProgress</span></span>
- <span data-ttu-id="0c609-135">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="0c609-135">Succeeded</span></span>
- <span data-ttu-id="0c609-136">Más</span><span class="sxs-lookup"><span data-stu-id="0c609-136">Other</span></span>
- <span data-ttu-id="0c609-137">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="0c609-137">Failed</span></span>
- <span data-ttu-id="0c609-138">Lemondott</span><span class="sxs-lookup"><span data-stu-id="0c609-138">Cancelled</span></span>
- <span data-ttu-id="0c609-139">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="0c609-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c609-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="0c609-140">-TargetObjectId</span></span>
<span data-ttu-id="0c609-141">Az objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c609-141">Specifies the ID of the object.</span></span> <span data-ttu-id="0c609-142">A megadott objektumon a feladatok keresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="0c609-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c609-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c609-143">CommonParameters</span></span>
<span data-ttu-id="0c609-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c609-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c609-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c609-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c609-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c609-146">INPUTS</span></span>

### <span data-ttu-id="0c609-147">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0c609-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0c609-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c609-148">OUTPUTS</span></span>

### <span data-ttu-id="0c609-149">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0c609-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0c609-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c609-150">NOTES</span></span>

## <span data-ttu-id="0c609-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c609-151">RELATED LINKS</span></span>

[<span data-ttu-id="0c609-152">Újraindítás – AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0c609-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0c609-153">Önéletrajz – AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0c609-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0c609-154">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0c609-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
