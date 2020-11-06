---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492164"
---
# <span data-ttu-id="2e303-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="2e303-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="2e303-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e303-102">SYNOPSIS</span></span>
<span data-ttu-id="2e303-103">Elindítja a nem tervezett feladatátvételt egy webhely-helyreállítási jogalanynál vagy helyreállítási tervben.</span><span class="sxs-lookup"><span data-stu-id="2e303-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e303-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e303-104">SYNTAX</span></span>

### <span data-ttu-id="2e303-105">ByPEObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e303-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e303-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="2e303-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e303-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="2e303-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e303-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e303-108">DESCRIPTION</span></span>
<span data-ttu-id="2e303-109">A **Start-AzureRmSiteRecoveryUnplannedFailoverJob** parancsmag az Azure webhely-helyreállítási védelem vagy helyreállítási terv nem tervezett feladatátvételét indítja el.</span><span class="sxs-lookup"><span data-stu-id="2e303-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="2e303-110">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmSiteRecoveryJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="2e303-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="2e303-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2e303-111">EXAMPLES</span></span>

## <span data-ttu-id="2e303-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e303-112">PARAMETERS</span></span>

### <span data-ttu-id="2e303-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="2e303-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="2e303-114">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e303-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="2e303-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="2e303-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="2e303-116">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e303-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="2e303-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e303-117">-DefaultProfile</span></span>
<span data-ttu-id="2e303-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e303-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e303-119">-Irány</span><span class="sxs-lookup"><span data-stu-id="2e303-119">-Direction</span></span>
<span data-ttu-id="2e303-120">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e303-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="2e303-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2e303-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e303-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="2e303-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="2e303-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="2e303-123">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e303-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="2e303-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="2e303-125">Azt jelzi, hogy a művelet a forrás-és a helyszíni műveleteket is elvégezheti.</span><span class="sxs-lookup"><span data-stu-id="2e303-125">Indicates that the action can perform source site operations.</span></span>

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

### <span data-ttu-id="2e303-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2e303-126">-ProtectionEntity</span></span>
<span data-ttu-id="2e303-127">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e303-127">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="2e303-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2e303-128">-RecoveryPlan</span></span>
<span data-ttu-id="2e303-129">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e303-129">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="2e303-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2e303-130">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e303-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e303-131">CommonParameters</span></span>
<span data-ttu-id="2e303-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e303-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e303-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e303-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e303-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e303-134">INPUTS</span></span>

### <span data-ttu-id="2e303-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2e303-135">ASRProtectionEntity</span></span>
<span data-ttu-id="2e303-136">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2e303-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="2e303-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2e303-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="2e303-138">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2e303-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="2e303-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2e303-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="2e303-140">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2e303-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="2e303-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e303-141">OUTPUTS</span></span>

### <span data-ttu-id="2e303-142">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2e303-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2e303-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e303-143">NOTES</span></span>

## <span data-ttu-id="2e303-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e303-144">RELATED LINKS</span></span>

[<span data-ttu-id="2e303-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2e303-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


