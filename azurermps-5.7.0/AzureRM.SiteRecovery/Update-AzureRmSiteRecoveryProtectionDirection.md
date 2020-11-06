---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: f7d8efcde5f60ed9cf6eb3aff7f86c9ea3171ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492161"
---
# <span data-ttu-id="f42c3-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="f42c3-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="f42c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f42c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f42c3-103">A forrás-és a célkiszolgáló frissítése egy webhely-helyreállítási objektum védelmére.</span><span class="sxs-lookup"><span data-stu-id="f42c3-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f42c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f42c3-104">SYNTAX</span></span>

### <span data-ttu-id="f42c3-105">ByPEObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f42c3-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f42c3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f42c3-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f42c3-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="f42c3-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f42c3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f42c3-108">DESCRIPTION</span></span>
<span data-ttu-id="f42c3-109">Az **Update-AzureRmSiteRecoveryProtectionDirection** parancsmag frissíti a forrás-és célkiszolgáló tartalmát az Azure-webhely helyreállítási objektumának védelmére a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="f42c3-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="f42c3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f42c3-110">EXAMPLES</span></span>

## <span data-ttu-id="f42c3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f42c3-111">PARAMETERS</span></span>

### <span data-ttu-id="f42c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42c3-112">-DefaultProfile</span></span>
<span data-ttu-id="f42c3-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f42c3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f42c3-114">-Irány</span><span class="sxs-lookup"><span data-stu-id="f42c3-114">-Direction</span></span>
<span data-ttu-id="f42c3-115">A véglegesítés irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f42c3-115">Specifies the direction of the commit.</span></span>
<span data-ttu-id="f42c3-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f42c3-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f42c3-117">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f42c3-117">PrimaryToRecovery</span></span>
- <span data-ttu-id="f42c3-118">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f42c3-118">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f42c3-119">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f42c3-119">-ProtectionEntity</span></span>
<span data-ttu-id="f42c3-120">A védelmi entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f42c3-120">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="f42c3-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f42c3-121">-RecoveryPlan</span></span>
<span data-ttu-id="f42c3-122">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f42c3-122">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="f42c3-123">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f42c3-123">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="f42c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42c3-124">CommonParameters</span></span>
<span data-ttu-id="f42c3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f42c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42c3-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f42c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42c3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f42c3-127">INPUTS</span></span>

### <span data-ttu-id="f42c3-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f42c3-128">ASRProtectionEntity</span></span>
<span data-ttu-id="f42c3-129">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f42c3-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="f42c3-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f42c3-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="f42c3-131">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f42c3-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="f42c3-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f42c3-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="f42c3-133">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f42c3-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="f42c3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f42c3-134">OUTPUTS</span></span>

### <span data-ttu-id="f42c3-135">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f42c3-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f42c3-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f42c3-136">NOTES</span></span>

## <span data-ttu-id="f42c3-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f42c3-137">RELATED LINKS</span></span>

