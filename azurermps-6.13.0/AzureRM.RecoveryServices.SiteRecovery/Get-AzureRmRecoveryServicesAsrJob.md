---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: f79bc9e32ab179c10c09f3780a591182ea1d630b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672906"
---
# <span data-ttu-id="c0f2c-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c0f2c-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c0f2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f2c-103">A megadott ASR-feladat részleteit vagy a legutóbbi ASR-feladatok listáját a helyreállítási szolgáltatások pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0f2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0f2c-104">SYNTAX</span></span>

### <span data-ttu-id="c0f2c-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0f2c-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0f2c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c0f2c-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0f2c-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="c0f2c-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f2c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="c0f2c-109">A **Get-AzureRmRecoveryServicesAsrJob** parancsmag Azure webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="c0f2c-110">Ezzel a parancsmaggal megtekintheti az ASR-feladatokat a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="c0f2c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c0f2c-111">EXAMPLES</span></span>

### <span data-ttu-id="c0f2c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0f2c-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="c0f2c-113">Egy adott ASR-objektum összes feladatát visszaadja (az ASR-objektumra (például a többszörözött elemre vagy a helyreállítási csomagra) az AZONOSÍTÓval.)</span><span class="sxs-lookup"><span data-stu-id="c0f2c-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="c0f2c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0f2c-114">PARAMETERS</span></span>

### <span data-ttu-id="c0f2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f2c-115">-DefaultProfile</span></span>
<span data-ttu-id="c0f2c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0f2c-117">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="c0f2c-117">-EndTime</span></span>
<span data-ttu-id="c0f2c-118">A feladatok befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="c0f2c-119">Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="c0f2c-120">Ha egy **datetime** objektumot szeretne beolvasni ehhez a paraméterhez, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="c0f2c-121">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c0f2c-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="c0f2c-122">-Job</span><span class="sxs-lookup"><span data-stu-id="c0f2c-122">-Job</span></span>
<span data-ttu-id="c0f2c-123">Az ASR-feladat objektumát adja meg, amely frissíti a részleteket.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="c0f2c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0f2c-124">-Name</span></span>
<span data-ttu-id="c0f2c-125">Adja meg az ASR-feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="c0f2c-126">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="c0f2c-126">-StartTime</span></span>
<span data-ttu-id="c0f2c-127">A feladatok kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="c0f2c-128">Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="c0f2c-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c0f2c-129">-State</span></span>
<span data-ttu-id="c0f2c-130">Az ASR-feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="c0f2c-131">Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="c0f2c-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c0f2c-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0f2c-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="c0f2c-133">NotStarted</span></span>
- <span data-ttu-id="c0f2c-134">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="c0f2c-134">InProgress</span></span>
- <span data-ttu-id="c0f2c-135">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="c0f2c-135">Succeeded</span></span>
- <span data-ttu-id="c0f2c-136">Más</span><span class="sxs-lookup"><span data-stu-id="c0f2c-136">Other</span></span>
- <span data-ttu-id="c0f2c-137">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="c0f2c-137">Failed</span></span>
- <span data-ttu-id="c0f2c-138">Lemondott</span><span class="sxs-lookup"><span data-stu-id="c0f2c-138">Cancelled</span></span>
- <span data-ttu-id="c0f2c-139">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="c0f2c-139">Suspended</span></span>

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

### <span data-ttu-id="c0f2c-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="c0f2c-140">-TargetObjectId</span></span>
<span data-ttu-id="c0f2c-141">Az objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-141">Specifies the ID of the object.</span></span> <span data-ttu-id="c0f2c-142">A megadott objektumon a feladatok keresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="c0f2c-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="c0f2c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f2c-143">CommonParameters</span></span>
<span data-ttu-id="c0f2c-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0f2c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f2c-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f2c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f2c-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0f2c-146">INPUTS</span></span>

### <span data-ttu-id="c0f2c-147">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c0f2c-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c0f2c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0f2c-148">OUTPUTS</span></span>

### <span data-ttu-id="c0f2c-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c0f2c-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c0f2c-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0f2c-150">NOTES</span></span>

## <span data-ttu-id="c0f2c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0f2c-151">RELATED LINKS</span></span>

[<span data-ttu-id="c0f2c-152">Újraindítás – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c0f2c-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c0f2c-153">Önéletrajz – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c0f2c-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c0f2c-154">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c0f2c-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
