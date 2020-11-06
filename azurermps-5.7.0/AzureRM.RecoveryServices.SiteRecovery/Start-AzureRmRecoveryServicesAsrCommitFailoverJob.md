---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: b491ede16973704f873e018a06ae6147df5cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492221"
---
# <span data-ttu-id="d336c-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d336c-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="d336c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d336c-102">SYNOPSIS</span></span>
<span data-ttu-id="d336c-103">Egy webhely-helyreállítási objektum véglegesítési feladatátvételi tevékenységének indítása.</span><span class="sxs-lookup"><span data-stu-id="d336c-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d336c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d336c-104">SYNTAX</span></span>

### <span data-ttu-id="d336c-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d336c-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d336c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d336c-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d336c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d336c-107">DESCRIPTION</span></span>
<span data-ttu-id="d336c-108">A **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** parancsmag a feladatátvételi művelet után egy Azure-webhely helyreállítási objektum véglegesítésének véglegesítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="d336c-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="d336c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d336c-109">EXAMPLES</span></span>

### <span data-ttu-id="d336c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d336c-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="d336c-111">Elindítja a megadott helyreállítási csomag véglegesítési feladatátvételét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d336c-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d336c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d336c-112">PARAMETERS</span></span>

### <span data-ttu-id="d336c-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d336c-113">-Confirm</span></span>
<span data-ttu-id="d336c-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d336c-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d336c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d336c-115">-DefaultProfile</span></span>
<span data-ttu-id="d336c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d336c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="d336c-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d336c-117">-RecoveryPlan</span></span>
<span data-ttu-id="d336c-118">A helyreállítási tervnek megfelelő ASR-helyreállítási terv objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d336c-118">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="d336c-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d336c-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d336c-120">Egy olyan ASR-replikációval védett elem objektumot ad meg, amely megfelel a replikációs védelemmel ellátott elemnek.</span><span class="sxs-lookup"><span data-stu-id="d336c-120">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="d336c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d336c-121">-WhatIf</span></span>
<span data-ttu-id="d336c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d336c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d336c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d336c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d336c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d336c-124">CommonParameters</span></span>
<span data-ttu-id="d336c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d336c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d336c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d336c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d336c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d336c-127">INPUTS</span></span>

### <span data-ttu-id="d336c-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d336c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="d336c-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d336c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d336c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d336c-130">OUTPUTS</span></span>

### <span data-ttu-id="d336c-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d336c-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d336c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d336c-132">NOTES</span></span>

## <span data-ttu-id="d336c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d336c-133">RELATED LINKS</span></span>
