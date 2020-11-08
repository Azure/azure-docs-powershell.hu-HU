---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016111"
---
# <span data-ttu-id="d6a0d-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6a0d-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="d6a0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a0d-103">Webhely-helyreállítási csomag eltávolítása a webhely-helyreállításból.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="d6a0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6a0d-104">SYNTAX</span></span>

### <span data-ttu-id="d6a0d-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6a0d-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6a0d-106">ById</span><span class="sxs-lookup"><span data-stu-id="d6a0d-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6a0d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a0d-108">A **Remove-AzureSiteRecoveryRecoveryPlan** parancsmag eltávolítja a webhely-helyreállítási csomagot az Azure jelenlegi helyreállítási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="d6a0d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6a0d-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a0d-110">1. példa: helyreállítási terv eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d6a0d-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="d6a0d-111">Az első parancs a **Get-AzureSiteRecoveryRecoveryPlan** parancsmagot használja a webhely-helyreállítási terv beszerzéséhez, majd a $RecoveryPlan változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="d6a0d-112">A második parancs eltávolítja az $RecoveryPlan helyreállítási tervét.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="d6a0d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6a0d-113">PARAMETERS</span></span>

### <span data-ttu-id="d6a0d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d6a0d-114">-Force</span></span>
<span data-ttu-id="d6a0d-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a0d-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d6a0d-116">-Id</span></span>
<span data-ttu-id="d6a0d-117">Az eltávolítandó helyreállítási terv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-117">Specifies the ID of the recovery plan to remove.</span></span>

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

### <span data-ttu-id="d6a0d-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="d6a0d-118">-Profile</span></span>
<span data-ttu-id="d6a0d-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6a0d-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6a0d-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6a0d-121">-RecoveryPlan</span></span>
<span data-ttu-id="d6a0d-122">Az eltávolítandó helyreállítási csomagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-122">Specifies the recovery plan to remove.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a0d-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d6a0d-123">-WaitForCompletion</span></span>
<span data-ttu-id="d6a0d-124">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a0d-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6a0d-125">-Confirm</span></span>
<span data-ttu-id="d6a0d-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a0d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a0d-127">-WhatIf</span></span>
<span data-ttu-id="d6a0d-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a0d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6a0d-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a0d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a0d-130">CommonParameters</span></span>
<span data-ttu-id="d6a0d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6a0d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a0d-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a0d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a0d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a0d-133">INPUTS</span></span>

## <span data-ttu-id="d6a0d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a0d-134">OUTPUTS</span></span>

## <span data-ttu-id="d6a0d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6a0d-135">NOTES</span></span>

## <span data-ttu-id="d6a0d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6a0d-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6a0d-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6a0d-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d6a0d-138">Új – AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6a0d-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d6a0d-139">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6a0d-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


