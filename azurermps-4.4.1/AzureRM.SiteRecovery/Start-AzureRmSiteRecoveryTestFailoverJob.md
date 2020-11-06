---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 330af3701741cbc83573afbbe7e283fdee294cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503168"
---
# <span data-ttu-id="300a0-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="300a0-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="300a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="300a0-102">SYNOPSIS</span></span>
<span data-ttu-id="300a0-103">Teszteli a feladatátvételt a webhely-helyreállítási védelem entitásban.</span><span class="sxs-lookup"><span data-stu-id="300a0-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="300a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="300a0-104">SYNTAX</span></span>

### <span data-ttu-id="300a0-105">ByPEObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="300a0-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="300a0-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="300a0-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="300a0-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="300a0-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="300a0-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="300a0-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="300a0-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a0-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="300a0-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="300a0-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="300a0-114">DESCRIPTION</span></span>
<span data-ttu-id="300a0-115">A **Start-AzureRmSiteRecoveryTestFailoverJob** parancsmag elindítja az Azure webhely-helyreállítási védelmi szervezet vagy helyreállítási terv feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="300a0-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="300a0-116">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmSiteRecoveryJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="300a0-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="300a0-117">Példák</span><span class="sxs-lookup"><span data-stu-id="300a0-117">EXAMPLES</span></span>

## <span data-ttu-id="300a0-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="300a0-118">PARAMETERS</span></span>

### <span data-ttu-id="300a0-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="300a0-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="300a0-120">Az Azure virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="300a0-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300a0-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="300a0-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="300a0-122">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="300a0-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="300a0-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="300a0-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="300a0-124">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="300a0-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="300a0-125">-Irány</span><span class="sxs-lookup"><span data-stu-id="300a0-125">-Direction</span></span>
<span data-ttu-id="300a0-126">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="300a0-126">Specifies the failover direction.</span></span>
<span data-ttu-id="300a0-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="300a0-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="300a0-128">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="300a0-128">PrimaryToRecovery</span></span>
- <span data-ttu-id="300a0-129">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="300a0-129">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="300a0-130">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="300a0-130">-ProtectionEntity</span></span>
<span data-ttu-id="300a0-131">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="300a0-131">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="300a0-132">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="300a0-132">-RecoveryPlan</span></span>
<span data-ttu-id="300a0-133">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="300a0-133">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="300a0-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="300a0-134">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="300a0-135">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="300a0-135">-VMNetwork</span></span>
<span data-ttu-id="300a0-136">A webhely-helyreállítási virtuális gép hálózatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="300a0-136">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300a0-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="300a0-137">-DefaultProfile</span></span>
<span data-ttu-id="300a0-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="300a0-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="300a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300a0-139">CommonParameters</span></span>
<span data-ttu-id="300a0-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="300a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300a0-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="300a0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300a0-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="300a0-142">INPUTS</span></span>

### <span data-ttu-id="300a0-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="300a0-143">ASRProtectionEntity</span></span>
<span data-ttu-id="300a0-144">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="300a0-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="300a0-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="300a0-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="300a0-146">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="300a0-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="300a0-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="300a0-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="300a0-148">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="300a0-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="300a0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="300a0-149">OUTPUTS</span></span>

### <span data-ttu-id="300a0-150">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="300a0-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="300a0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="300a0-151">NOTES</span></span>

## <span data-ttu-id="300a0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="300a0-152">RELATED LINKS</span></span>

[<span data-ttu-id="300a0-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="300a0-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
