---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 08e864c3d95c4d077e4d9e1227a0ec606508c193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494642"
---
# <span data-ttu-id="5c426-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5c426-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="5c426-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c426-102">SYNOPSIS</span></span>
<span data-ttu-id="5c426-103">Egy webhely-helyreállítási objektum véglegesítési feladatátvételi tevékenységének indítása.</span><span class="sxs-lookup"><span data-stu-id="5c426-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c426-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c426-104">SYNTAX</span></span>

### <span data-ttu-id="5c426-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c426-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c426-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5c426-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c426-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="5c426-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c426-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c426-108">DESCRIPTION</span></span>
<span data-ttu-id="5c426-109">A **Start-AzureRmSiteRecoveryCommitFailoverJob** parancsmag a feladatátvételi művelet után egy Azure-webhely helyreállítási objektum véglegesítésének véglegesítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="5c426-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="5c426-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5c426-110">EXAMPLES</span></span>

## <span data-ttu-id="5c426-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c426-111">PARAMETERS</span></span>

### <span data-ttu-id="5c426-112">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5c426-112">-ProtectionEntity</span></span>
<span data-ttu-id="5c426-113">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c426-113">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c426-114">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5c426-114">-RecoveryPlan</span></span>
<span data-ttu-id="5c426-115">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c426-115">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c426-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c426-116">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c426-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c426-117">-DefaultProfile</span></span>
<span data-ttu-id="5c426-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c426-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c426-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c426-119">CommonParameters</span></span>
<span data-ttu-id="5c426-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c426-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c426-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c426-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c426-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c426-122">INPUTS</span></span>

### <span data-ttu-id="5c426-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5c426-123">ASRProtectionEntity</span></span>
<span data-ttu-id="5c426-124">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5c426-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="5c426-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5c426-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="5c426-126">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5c426-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="5c426-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c426-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="5c426-128">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5c426-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="5c426-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c426-129">OUTPUTS</span></span>

### <span data-ttu-id="5c426-130">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c426-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c426-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c426-131">NOTES</span></span>

## <span data-ttu-id="5c426-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c426-132">RELATED LINKS</span></span>

