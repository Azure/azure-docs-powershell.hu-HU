---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016407"
---
# <span data-ttu-id="d1b42-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d1b42-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="d1b42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1b42-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b42-103">Webhely-helyreállítási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="d1b42-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="d1b42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1b42-104">SYNTAX</span></span>

### <span data-ttu-id="d1b42-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1b42-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d1b42-106">ById</span><span class="sxs-lookup"><span data-stu-id="d1b42-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d1b42-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1b42-107">DESCRIPTION</span></span>
<span data-ttu-id="d1b42-108">A **stop-AzureSiteRecoveryJob** parancsmag leállítja az Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="d1b42-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="d1b42-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d1b42-109">EXAMPLES</span></span>

### <span data-ttu-id="d1b42-110">Példa 1: az összes feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="d1b42-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="d1b42-111">Az első parancs a **Get-AzureSiteRecoveryJob** parancsmag használatával megkapja az Azure webhely-helyreállítási feladatokat az aktuális Azure webhely-helyreállítási tárolóhoz, majd a $Jobs változóban tárolja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="d1b42-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="d1b42-112">A második parancs leállítja az $Jobs által megadott feladatokat.</span><span class="sxs-lookup"><span data-stu-id="d1b42-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="d1b42-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1b42-113">PARAMETERS</span></span>

### <span data-ttu-id="d1b42-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d1b42-114">-Id</span></span>
<span data-ttu-id="d1b42-115">A leállításhoz adja meg a feladat AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="d1b42-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="d1b42-116">-Job</span><span class="sxs-lookup"><span data-stu-id="d1b42-116">-Job</span></span>
<span data-ttu-id="d1b42-117">A leállítási feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1b42-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="d1b42-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="d1b42-118">-Profile</span></span>
<span data-ttu-id="d1b42-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d1b42-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1b42-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d1b42-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d1b42-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b42-121">CommonParameters</span></span>
<span data-ttu-id="d1b42-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1b42-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b42-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b42-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b42-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1b42-124">INPUTS</span></span>

## <span data-ttu-id="d1b42-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1b42-125">OUTPUTS</span></span>

## <span data-ttu-id="d1b42-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1b42-126">NOTES</span></span>

## <span data-ttu-id="d1b42-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1b42-127">RELATED LINKS</span></span>

[<span data-ttu-id="d1b42-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d1b42-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d1b42-129">Újraindítás – AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d1b42-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d1b42-130">Önéletrajz – AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d1b42-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


