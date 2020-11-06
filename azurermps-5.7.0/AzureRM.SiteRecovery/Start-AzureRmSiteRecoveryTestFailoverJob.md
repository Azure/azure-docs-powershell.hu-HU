---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492999"
---
# <span data-ttu-id="19983-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="19983-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="19983-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19983-102">SYNOPSIS</span></span>
<span data-ttu-id="19983-103">Teszteli a feladatátvételt a webhely-helyreállítási védelem entitásban.</span><span class="sxs-lookup"><span data-stu-id="19983-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19983-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19983-104">SYNTAX</span></span>

### <span data-ttu-id="19983-105">ByPEObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19983-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="19983-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="19983-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="19983-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="19983-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="19983-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="19983-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="19983-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19983-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="19983-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19983-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="19983-114">DESCRIPTION</span></span>
<span data-ttu-id="19983-115">A **Start-AzureRmSiteRecoveryTestFailoverJob** parancsmag elindítja az Azure webhely-helyreállítási védelmi szervezet vagy helyreállítási terv feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="19983-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="19983-116">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmSiteRecoveryJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="19983-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="19983-117">Példák</span><span class="sxs-lookup"><span data-stu-id="19983-117">EXAMPLES</span></span>

## <span data-ttu-id="19983-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19983-118">PARAMETERS</span></span>

### <span data-ttu-id="19983-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="19983-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="19983-120">Az Azure virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19983-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19983-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="19983-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="19983-122">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19983-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="19983-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="19983-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="19983-124">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19983-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="19983-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19983-125">-DefaultProfile</span></span>
<span data-ttu-id="19983-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19983-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19983-127">-Irány</span><span class="sxs-lookup"><span data-stu-id="19983-127">-Direction</span></span>
<span data-ttu-id="19983-128">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="19983-128">Specifies the failover direction.</span></span>
<span data-ttu-id="19983-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="19983-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19983-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="19983-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="19983-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="19983-131">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="19983-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="19983-132">-ProtectionEntity</span></span>
<span data-ttu-id="19983-133">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="19983-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19983-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="19983-134">-RecoveryPlan</span></span>
<span data-ttu-id="19983-135">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="19983-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19983-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="19983-136">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19983-137">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="19983-137">-VMNetwork</span></span>
<span data-ttu-id="19983-138">A webhely-helyreállítási virtuális gép hálózatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="19983-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19983-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19983-139">CommonParameters</span></span>
<span data-ttu-id="19983-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19983-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19983-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19983-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19983-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19983-142">INPUTS</span></span>

### <span data-ttu-id="19983-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="19983-143">ASRProtectionEntity</span></span>
<span data-ttu-id="19983-144">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="19983-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="19983-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="19983-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="19983-146">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="19983-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="19983-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="19983-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="19983-148">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="19983-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="19983-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19983-149">OUTPUTS</span></span>

### <span data-ttu-id="19983-150">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="19983-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="19983-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19983-151">NOTES</span></span>

## <span data-ttu-id="19983-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19983-152">RELATED LINKS</span></span>

[<span data-ttu-id="19983-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="19983-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
