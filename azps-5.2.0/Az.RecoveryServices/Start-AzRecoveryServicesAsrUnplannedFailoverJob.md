---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330821"
---
# <span data-ttu-id="1ad3f-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1ad3f-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="1ad3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad3f-103">Nem tervezett feladatátvételi műveletet kezd.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="1ad3f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ad3f-104">SYNTAX</span></span>

### <span data-ttu-id="1ad3f-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ad3f-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad3f-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1ad3f-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad3f-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="1ad3f-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad3f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ad3f-108">DESCRIPTION</span></span>
<span data-ttu-id="1ad3f-109">A **Start-AzRecoveryServicesAsrUnplannedFailoverService** parancsmag nem tervezett feladatátvételt indít az Azure-webhely-helyreállítási replikációval védett elem vagy helyreállítási terv esetében.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="1ad3f-110">A feladat sikeres voltának ellenőrzéséhez használja a Get-AzRecoveryServicesAsrJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="1ad3f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ad3f-111">EXAMPLES</span></span>

### <span data-ttu-id="1ad3f-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ad3f-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="1ad3f-113">Elindítja a helyreállítási terv nem tervezett feladatátvételi műveletét a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1ad3f-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="1ad3f-114">Example 2</span></span>

<span data-ttu-id="1ad3f-115">Nem tervezett feladatátvételi műveletet kezd.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="1ad3f-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="1ad3f-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="1ad3f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ad3f-117">PARAMETERS</span></span>

### <span data-ttu-id="1ad3f-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1ad3f-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1ad3f-119">A védett elem feladatátvételéhez szükséges elsődleges tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1ad3f-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1ad3f-121">A védett elem feladatátvételéhez szükséges adattitkosítási másodlagos tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad3f-122">-DefaultProfile</span></span>
<span data-ttu-id="1ad3f-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1ad3f-124">-Irány</span><span class="sxs-lookup"><span data-stu-id="1ad3f-124">-Direction</span></span>
<span data-ttu-id="1ad3f-125">A feladatátvétel irányát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-125">Specifies the failover direction.</span></span>
<span data-ttu-id="1ad3f-126">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="1ad3f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ad3f-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1ad3f-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="1ad3f-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1ad3f-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="1ad3f-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="1ad3f-130">A nem tervezett feladatátvétel megkezdése előtt végezze el a műveletet a forrásoldalon.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-130">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1ad3f-131">-RecoveryPlan</span></span>
<span data-ttu-id="1ad3f-132">Egy ASR helyreállítási tervobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-132">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1ad3f-133">-RecoveryPoint</span></span>
<span data-ttu-id="1ad3f-134">Egy egyéni helyreállítási pontot ad meg, amely feladatátvételt nyújt a védett gépnek.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="1ad3f-135">-RecoveryTag</span></span>
<span data-ttu-id="1ad3f-136">Azt a helyreállítási címkét adja meg, amelybe a feladatátvételt el kell látni.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-136">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ad3f-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1ad3f-138">Egy azure-webhely-helyreállítási replikációval védett elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-138">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ad3f-139">-Confirm</span></span>
<span data-ttu-id="1ad3f-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad3f-141">-WhatIf</span></span>
<span data-ttu-id="1ad3f-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ad3f-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad3f-144">CommonParameters</span></span>
<span data-ttu-id="1ad3f-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad3f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad3f-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ad3f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad3f-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ad3f-147">INPUTS</span></span>

### <span data-ttu-id="1ad3f-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1ad3f-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="1ad3f-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ad3f-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1ad3f-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad3f-150">OUTPUTS</span></span>

### <span data-ttu-id="1ad3f-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="1ad3f-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1ad3f-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ad3f-152">NOTES</span></span>

## <span data-ttu-id="1ad3f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ad3f-153">RELATED LINKS</span></span>

[<span data-ttu-id="1ad3f-154">Get-AzRecoveryServicesAsrService</span><span class="sxs-lookup"><span data-stu-id="1ad3f-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
