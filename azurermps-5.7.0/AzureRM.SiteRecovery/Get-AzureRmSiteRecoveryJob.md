---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498780"
---
# <span data-ttu-id="66a21-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="66a21-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="66a21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66a21-102">SYNOPSIS</span></span>
<span data-ttu-id="66a21-103">Az aktuális webhely-helyreállítási boltozat üzemeltetési adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66a21-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66a21-104">SYNTAX</span></span>

### <span data-ttu-id="66a21-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66a21-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a21-106">ByName</span><span class="sxs-lookup"><span data-stu-id="66a21-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a21-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="66a21-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a21-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="66a21-108">DESCRIPTION</span></span>
<span data-ttu-id="66a21-109">A **Get-AzureRmSiteRecoveryJob** parancsmag Azure webhely-helyreállítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="66a21-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="66a21-110">Ezzel a parancsmaggal megtekintheti az aktuális webhely-helyreállítási boltozat üzemeltetési adatait.</span><span class="sxs-lookup"><span data-stu-id="66a21-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="66a21-111">Példák</span><span class="sxs-lookup"><span data-stu-id="66a21-111">EXAMPLES</span></span>

## <span data-ttu-id="66a21-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66a21-112">PARAMETERS</span></span>

### <span data-ttu-id="66a21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a21-113">-DefaultProfile</span></span>
<span data-ttu-id="66a21-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66a21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a21-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="66a21-115">-EndTime</span></span>
<span data-ttu-id="66a21-116">A feladatok befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="66a21-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="66a21-117">Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="66a21-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="66a21-118">Ha egy **datetime** objektumot szeretne beolvasni ehhez a paraméterhez, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="66a21-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="66a21-119">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="66a21-119">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="66a21-120">-Job</span><span class="sxs-lookup"><span data-stu-id="66a21-120">-Job</span></span>
<span data-ttu-id="66a21-121">A webhely-helyreállítási feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="66a21-121">Specifies the Site Recovery job.</span></span>

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

### <span data-ttu-id="66a21-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66a21-122">-Name</span></span>
<span data-ttu-id="66a21-123">Megadja a feladatot azonosító egyedi nevet.</span><span class="sxs-lookup"><span data-stu-id="66a21-123">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="66a21-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="66a21-124">-StartTime</span></span>
<span data-ttu-id="66a21-125">A feladatok kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="66a21-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="66a21-126">Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.</span><span class="sxs-lookup"><span data-stu-id="66a21-126">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="66a21-127">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="66a21-127">-State</span></span>
<span data-ttu-id="66a21-128">A webhely-helyreállítási feladatok beviteli állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="66a21-128">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="66a21-129">Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="66a21-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="66a21-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="66a21-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66a21-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="66a21-131">NotStarted</span></span>
- <span data-ttu-id="66a21-132">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="66a21-132">InProgress</span></span>
- <span data-ttu-id="66a21-133">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="66a21-133">Succeeded</span></span>
- <span data-ttu-id="66a21-134">Más</span><span class="sxs-lookup"><span data-stu-id="66a21-134">Other</span></span>
- <span data-ttu-id="66a21-135">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="66a21-135">Failed</span></span>
- <span data-ttu-id="66a21-136">Lemondott</span><span class="sxs-lookup"><span data-stu-id="66a21-136">Cancelled</span></span>
- <span data-ttu-id="66a21-137">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="66a21-137">Suspended</span></span>

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

### <span data-ttu-id="66a21-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="66a21-138">-TargetObjectId</span></span>
<span data-ttu-id="66a21-139">A feladat által célzott objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="66a21-139">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="66a21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a21-140">CommonParameters</span></span>
<span data-ttu-id="66a21-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66a21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a21-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a21-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a21-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66a21-143">INPUTS</span></span>

### <span data-ttu-id="66a21-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="66a21-144">ASRJob</span></span>
<span data-ttu-id="66a21-145">A ' Job ' paraméter elfogadja a "ASRJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="66a21-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="66a21-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66a21-146">OUTPUTS</span></span>

### <span data-ttu-id="66a21-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="66a21-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="66a21-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66a21-148">NOTES</span></span>

## <span data-ttu-id="66a21-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66a21-149">RELATED LINKS</span></span>

[<span data-ttu-id="66a21-150">Újraindítás – AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="66a21-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="66a21-151">Önéletrajz – AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="66a21-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="66a21-152">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="66a21-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
