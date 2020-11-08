---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015585"
---
# <span data-ttu-id="a29a4-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a29a4-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="a29a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a29a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a29a4-103">Helyreállítási csomagot kap a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="a29a4-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="a29a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a29a4-104">SYNTAX</span></span>

### <span data-ttu-id="a29a4-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a29a4-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a29a4-106">ById</span><span class="sxs-lookup"><span data-stu-id="a29a4-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a29a4-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a29a4-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a29a4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a29a4-108">DESCRIPTION</span></span>
<span data-ttu-id="a29a4-109">A **Get-AzureSiteRecoveryRecoveryPlan** parancsmag helyreállítási csomagot kap az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="a29a4-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="a29a4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a29a4-110">EXAMPLES</span></span>

### <span data-ttu-id="a29a4-111">Példa 1: helyreállítási terv beszerzése</span><span class="sxs-lookup"><span data-stu-id="a29a4-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="a29a4-112">Ez a parancs információt kap az Azure-webhely jelenlegi helyreállítási boltozatának helyreállítási tervéről.</span><span class="sxs-lookup"><span data-stu-id="a29a4-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a29a4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a29a4-113">PARAMETERS</span></span>

### <span data-ttu-id="a29a4-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a29a4-114">-Id</span></span>
<span data-ttu-id="a29a4-115">A beszerzési terv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a29a4-115">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a29a4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a29a4-116">-Name</span></span>
<span data-ttu-id="a29a4-117">A beolvasott helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a29a4-117">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a29a4-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="a29a4-118">-Profile</span></span>
<span data-ttu-id="a29a4-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a29a4-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a29a4-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a29a4-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a29a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29a4-121">CommonParameters</span></span>
<span data-ttu-id="a29a4-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a29a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29a4-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a29a4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29a4-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a29a4-124">INPUTS</span></span>

## <span data-ttu-id="a29a4-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a29a4-125">OUTPUTS</span></span>

## <span data-ttu-id="a29a4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a29a4-126">NOTES</span></span>

## <span data-ttu-id="a29a4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a29a4-127">RELATED LINKS</span></span>

[<span data-ttu-id="a29a4-128">Új – AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a29a4-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a29a4-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a29a4-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a29a4-130">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a29a4-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


