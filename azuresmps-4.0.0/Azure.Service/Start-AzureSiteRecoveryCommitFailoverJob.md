---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015778"
---
# <span data-ttu-id="646a6-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="646a6-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="646a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="646a6-102">SYNOPSIS</span></span>
<span data-ttu-id="646a6-103">Egy webhely-helyreállítási objektum véglegesítési feladatátvételi tevékenységének indítása.</span><span class="sxs-lookup"><span data-stu-id="646a6-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="646a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="646a6-104">SYNTAX</span></span>

### <span data-ttu-id="646a6-105">ByRPId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="646a6-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="646a6-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="646a6-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="646a6-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="646a6-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="646a6-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="646a6-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="646a6-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="646a6-109">DESCRIPTION</span></span>
<span data-ttu-id="646a6-110">A **Start-AzureSiteRecoveryCommitFailoverJob** parancsmag a feladatátvételi művelet után egy Azure-webhely helyreállítási objektum véglegesítésének véglegesítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="646a6-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="646a6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="646a6-111">EXAMPLES</span></span>

### <span data-ttu-id="646a6-112">Példa 1: véglegesítési feladatátvételi feladat indítása</span><span class="sxs-lookup"><span data-stu-id="646a6-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="646a6-113">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmaggal minden védett tárolót megkapja az aktuális Azure-webhely helyreállítási boltozatához, majd a $Container változóban tárolja a találatokat.</span><span class="sxs-lookup"><span data-stu-id="646a6-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="646a6-114">A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmaggal a $Container tárolt tárolóhoz tartozó védett virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="646a6-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="646a6-115">A parancs az eredményt a $Protected változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="646a6-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="646a6-116">A végleges parancs elindítja a feladatátvételi feladatot az $Protected tárolt védett objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="646a6-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="646a6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="646a6-117">PARAMETERS</span></span>

### <span data-ttu-id="646a6-118">-Irány</span><span class="sxs-lookup"><span data-stu-id="646a6-118">-Direction</span></span>
<span data-ttu-id="646a6-119">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="646a6-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="646a6-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="646a6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="646a6-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="646a6-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="646a6-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="646a6-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="646a6-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="646a6-123">-Profile</span></span>
<span data-ttu-id="646a6-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="646a6-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="646a6-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="646a6-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="646a6-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="646a6-126">-ProtectionContainerId</span></span>
<span data-ttu-id="646a6-127">Egy védett tároló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="646a6-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="646a6-128">Ez a parancsmag elindítja a feladatot egy olyan védett virtuális géphez, amely a parancsmag által megadott tárolóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="646a6-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646a6-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="646a6-129">-ProtectionEntity</span></span>
<span data-ttu-id="646a6-130">Azt a **ASRProtectionEntity** -objektumot adja meg, amelybe a feladatot el szeretné kezdeni.</span><span class="sxs-lookup"><span data-stu-id="646a6-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="646a6-131">Ha **ASRProtectionEntity** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryProtectionEntity** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="646a6-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="646a6-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="646a6-132">-ProtectionEntityId</span></span>
<span data-ttu-id="646a6-133">Annak a védett virtuális gépnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="646a6-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646a6-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="646a6-134">-RecoveryPlan</span></span>
<span data-ttu-id="646a6-135">Annak a helyreállítási tervnek az objektumát adja meg, amelybe a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="646a6-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="646a6-136">Ha **ASRRecoveryPlan** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryRecoveryPlan** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="646a6-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="646a6-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="646a6-137">-RPId</span></span>
<span data-ttu-id="646a6-138">Annak a helyreállítási tervnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="646a6-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646a6-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="646a6-139">-WaitForCompletion</span></span>
<span data-ttu-id="646a6-140">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="646a6-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="646a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646a6-141">CommonParameters</span></span>
<span data-ttu-id="646a6-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="646a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646a6-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="646a6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646a6-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="646a6-144">INPUTS</span></span>

## <span data-ttu-id="646a6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="646a6-145">OUTPUTS</span></span>

## <span data-ttu-id="646a6-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="646a6-146">NOTES</span></span>

## <span data-ttu-id="646a6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="646a6-147">RELATED LINKS</span></span>

[<span data-ttu-id="646a6-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="646a6-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="646a6-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="646a6-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="646a6-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="646a6-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


