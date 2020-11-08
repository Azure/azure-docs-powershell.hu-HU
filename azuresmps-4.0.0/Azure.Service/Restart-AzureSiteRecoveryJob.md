---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016076"
---
# <span data-ttu-id="9b455-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9b455-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="9b455-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b455-102">SYNOPSIS</span></span>
<span data-ttu-id="9b455-103">Webhely-helyreállítási feladat újraindítása.</span><span class="sxs-lookup"><span data-stu-id="9b455-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="9b455-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b455-104">SYNTAX</span></span>

### <span data-ttu-id="9b455-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b455-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9b455-106">ById</span><span class="sxs-lookup"><span data-stu-id="9b455-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9b455-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b455-107">DESCRIPTION</span></span>
<span data-ttu-id="9b455-108">Az **Újraindítás – AzureSiteRecoveryJob** parancsmag újraindítja az Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="9b455-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9b455-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9b455-109">EXAMPLES</span></span>

### <span data-ttu-id="9b455-110">Példa 1: feladat újraindítása</span><span class="sxs-lookup"><span data-stu-id="9b455-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="9b455-111">Ez a parancs elindítja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="9b455-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="9b455-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b455-112">PARAMETERS</span></span>

### <span data-ttu-id="9b455-113">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9b455-113">-Id</span></span>
<span data-ttu-id="9b455-114">Az újraindítani kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b455-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="9b455-115">-Job</span><span class="sxs-lookup"><span data-stu-id="9b455-115">-Job</span></span>
<span data-ttu-id="9b455-116">Az újraindítani kívánt feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b455-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="9b455-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="9b455-117">-Profile</span></span>
<span data-ttu-id="9b455-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9b455-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b455-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9b455-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b455-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b455-120">CommonParameters</span></span>
<span data-ttu-id="9b455-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b455-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b455-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b455-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b455-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b455-123">INPUTS</span></span>

## <span data-ttu-id="9b455-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b455-124">OUTPUTS</span></span>

## <span data-ttu-id="9b455-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b455-125">NOTES</span></span>

## <span data-ttu-id="9b455-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b455-126">RELATED LINKS</span></span>

[<span data-ttu-id="9b455-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9b455-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9b455-128">Önéletrajz – AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9b455-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9b455-129">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9b455-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


