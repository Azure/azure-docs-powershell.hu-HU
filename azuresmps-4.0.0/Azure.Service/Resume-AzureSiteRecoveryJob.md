---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016440"
---
# <span data-ttu-id="ef019-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ef019-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="ef019-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef019-102">SYNOPSIS</span></span>
<span data-ttu-id="ef019-103">Folytatja a felfüggesztett webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="ef019-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="ef019-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef019-104">SYNTAX</span></span>

### <span data-ttu-id="ef019-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef019-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ef019-106">ById</span><span class="sxs-lookup"><span data-stu-id="ef019-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ef019-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef019-107">DESCRIPTION</span></span>
<span data-ttu-id="ef019-108">A **resume-AzureSiteRecoveryJob** parancsmag folytatja a felfüggesztett Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="ef019-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="ef019-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef019-109">EXAMPLES</span></span>

### <span data-ttu-id="ef019-110">Példa 1: az összes feladat folytatása</span><span class="sxs-lookup"><span data-stu-id="ef019-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="ef019-111">Az első parancs a **Get-AzureSiteRecoveryJob** parancsmag használatával megkapja az összes Azure webhely-helyreállítási munkahelyet az aktuális webhely-helyreállítási tárolóhoz, majd a $Jobs változóban tárolja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="ef019-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="ef019-112">A második parancs a $Jobs által megadott feladatot folytatja.</span><span class="sxs-lookup"><span data-stu-id="ef019-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="ef019-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef019-113">PARAMETERS</span></span>

### <span data-ttu-id="ef019-114">-Megjegyzések</span><span class="sxs-lookup"><span data-stu-id="ef019-114">-Comments</span></span>
<span data-ttu-id="ef019-115">A Projektnapló megjegyzéseit adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef019-115">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef019-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ef019-116">-Id</span></span>
<span data-ttu-id="ef019-117">Egy feladat AZONOSÍTÓját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ef019-117">Specifies the ID of a job to resume.</span></span>

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

### <span data-ttu-id="ef019-118">-Job</span><span class="sxs-lookup"><span data-stu-id="ef019-118">-Job</span></span>
<span data-ttu-id="ef019-119">Adja meg, hogy milyen feladatot szeretne folytatni.</span><span class="sxs-lookup"><span data-stu-id="ef019-119">Specifies the job to resume.</span></span>

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

### <span data-ttu-id="ef019-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="ef019-120">-Profile</span></span>
<span data-ttu-id="ef019-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ef019-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef019-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ef019-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef019-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef019-123">CommonParameters</span></span>
<span data-ttu-id="ef019-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef019-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef019-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef019-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef019-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef019-126">INPUTS</span></span>

## <span data-ttu-id="ef019-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef019-127">OUTPUTS</span></span>

## <span data-ttu-id="ef019-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef019-128">NOTES</span></span>

## <span data-ttu-id="ef019-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef019-129">RELATED LINKS</span></span>

[<span data-ttu-id="ef019-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ef019-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="ef019-131">Újraindítás – AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ef019-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="ef019-132">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ef019-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


