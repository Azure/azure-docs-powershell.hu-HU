---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672401"
---
# <span data-ttu-id="23ea2-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="23ea2-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="23ea2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="23ea2-103">Az aktuális webhely-helyreállítási boltozat üzemeltetési adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="23ea2-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23ea2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23ea2-104">SYNTAX</span></span>

### <span data-ttu-id="23ea2-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23ea2-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ea2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="23ea2-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ea2-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="23ea2-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23ea2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="23ea2-108">DESCRIPTION</span></span>
<span data-ttu-id="23ea2-109">A **Get-AzureRmSiteRecoveryJob** parancsmag Azure webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="23ea2-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="23ea2-110">Ezzel a parancsmaggal megtekintheti az aktuális webhely-helyreállítási boltozat üzemeltetési adatait.</span><span class="sxs-lookup"><span data-stu-id="23ea2-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="23ea2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="23ea2-111">EXAMPLES</span></span>

## <span data-ttu-id="23ea2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23ea2-112">PARAMETERS</span></span>

### <span data-ttu-id="23ea2-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="23ea2-113">-EndTime</span></span>
<span data-ttu-id="23ea2-114">A feladatok befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="23ea2-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="23ea2-115">Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="23ea2-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="23ea2-116">Ha egy **datetime** objektumot szeretne beolvasni ehhez a paraméterhez, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="23ea2-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="23ea2-117">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="23ea2-117">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="23ea2-118">-Job</span><span class="sxs-lookup"><span data-stu-id="23ea2-118">-Job</span></span>
<span data-ttu-id="23ea2-119">A webhely-helyreállítási feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="23ea2-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ea2-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23ea2-120">-Name</span></span>
<span data-ttu-id="23ea2-121">Megadja a feladatot azonosító egyedi nevet.</span><span class="sxs-lookup"><span data-stu-id="23ea2-121">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="23ea2-122">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="23ea2-122">-StartTime</span></span>
<span data-ttu-id="23ea2-123">A feladatok kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="23ea2-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="23ea2-124">Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.</span><span class="sxs-lookup"><span data-stu-id="23ea2-124">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="23ea2-125">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="23ea2-125">-State</span></span>
<span data-ttu-id="23ea2-126">A webhely-helyreállítási feladatok beviteli állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="23ea2-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="23ea2-127">Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="23ea2-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="23ea2-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="23ea2-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23ea2-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="23ea2-129">NotStarted</span></span>
- <span data-ttu-id="23ea2-130">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="23ea2-130">InProgress</span></span>
- <span data-ttu-id="23ea2-131">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="23ea2-131">Succeeded</span></span>
- <span data-ttu-id="23ea2-132">Más</span><span class="sxs-lookup"><span data-stu-id="23ea2-132">Other</span></span>
- <span data-ttu-id="23ea2-133">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="23ea2-133">Failed</span></span>
- <span data-ttu-id="23ea2-134">Lemondott</span><span class="sxs-lookup"><span data-stu-id="23ea2-134">Cancelled</span></span>
- <span data-ttu-id="23ea2-135">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="23ea2-135">Suspended</span></span>

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

### <span data-ttu-id="23ea2-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="23ea2-136">-TargetObjectId</span></span>
<span data-ttu-id="23ea2-137">A feladat által célzott objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="23ea2-137">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="23ea2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ea2-138">-DefaultProfile</span></span>
<span data-ttu-id="23ea2-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23ea2-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23ea2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ea2-140">CommonParameters</span></span>
<span data-ttu-id="23ea2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23ea2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ea2-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ea2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ea2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23ea2-143">INPUTS</span></span>

### <span data-ttu-id="23ea2-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="23ea2-144">ASRJob</span></span>
<span data-ttu-id="23ea2-145">A ' Job ' paraméter elfogadja a "ASRJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="23ea2-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="23ea2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23ea2-146">OUTPUTS</span></span>

### <span data-ttu-id="23ea2-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="23ea2-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="23ea2-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23ea2-148">NOTES</span></span>

## <span data-ttu-id="23ea2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23ea2-149">RELATED LINKS</span></span>

[<span data-ttu-id="23ea2-150">Újraindítás – AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="23ea2-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="23ea2-151">Önéletrajz – AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="23ea2-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="23ea2-152">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="23ea2-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
