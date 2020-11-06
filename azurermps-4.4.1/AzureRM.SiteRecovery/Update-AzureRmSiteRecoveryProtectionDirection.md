---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494632"
---
# <span data-ttu-id="257cd-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="257cd-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="257cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="257cd-102">SYNOPSIS</span></span>
<span data-ttu-id="257cd-103">A forrás-és a célkiszolgáló frissítése egy webhely-helyreállítási objektum védelmére.</span><span class="sxs-lookup"><span data-stu-id="257cd-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="257cd-104">SYNTAX</span></span>

### <span data-ttu-id="257cd-105">ByPEObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="257cd-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="257cd-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="257cd-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="257cd-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="257cd-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="257cd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="257cd-108">DESCRIPTION</span></span>
<span data-ttu-id="257cd-109">Az **Update-AzureRmSiteRecoveryProtectionDirection** parancsmag frissíti a forrás-és célkiszolgáló tartalmát az Azure-webhely helyreállítási objektumának védelmére a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="257cd-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="257cd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="257cd-110">EXAMPLES</span></span>

## <span data-ttu-id="257cd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="257cd-111">PARAMETERS</span></span>

### <span data-ttu-id="257cd-112">-Irány</span><span class="sxs-lookup"><span data-stu-id="257cd-112">-Direction</span></span>
<span data-ttu-id="257cd-113">A véglegesítés irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="257cd-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="257cd-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="257cd-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="257cd-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="257cd-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="257cd-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="257cd-116">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="257cd-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="257cd-117">-ProtectionEntity</span></span>
<span data-ttu-id="257cd-118">A védelmi entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="257cd-118">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="257cd-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="257cd-119">-RecoveryPlan</span></span>
<span data-ttu-id="257cd-120">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="257cd-120">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="257cd-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="257cd-121">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="257cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257cd-122">-DefaultProfile</span></span>
<span data-ttu-id="257cd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="257cd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="257cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257cd-124">CommonParameters</span></span>
<span data-ttu-id="257cd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="257cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257cd-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257cd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257cd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="257cd-127">INPUTS</span></span>

### <span data-ttu-id="257cd-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="257cd-128">ASRProtectionEntity</span></span>
<span data-ttu-id="257cd-129">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="257cd-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="257cd-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="257cd-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="257cd-131">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="257cd-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="257cd-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="257cd-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="257cd-133">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="257cd-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="257cd-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="257cd-134">OUTPUTS</span></span>

### <span data-ttu-id="257cd-135">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="257cd-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="257cd-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="257cd-136">NOTES</span></span>

## <span data-ttu-id="257cd-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="257cd-137">RELATED LINKS</span></span>

