---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492222"
---
# <span data-ttu-id="e6cc3-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e6cc3-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="e6cc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cc3-103">A feladatátvételi művelet véglegesítése előtt módosítja a sikertelenül védett elem helyreállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6cc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6cc3-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6cc3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cc3-106">A **kezdő AzureRmRecoveryServicesAsrApplyRecoveryPoint** a sikertelenül védett elem helyreállítási pontját a feladatátvételi művelet véglegesítése előtt módosítja.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="e6cc3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cc3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6cc3-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="e6cc3-109">A megadott helyreállítási pont alkalmazása a replikációs védelemmel ellátott elemre, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e6cc3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6cc3-110">PARAMETERS</span></span>

### <span data-ttu-id="e6cc3-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6cc3-111">-Confirm</span></span>
<span data-ttu-id="e6cc3-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6cc3-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e6cc3-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e6cc3-114">Az elsődleges tanúsítványfájl megadása, ha az adattitkosítást használják.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-114">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="e6cc3-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e6cc3-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e6cc3-116">Megadja a másodlagos tanúsítványfájl-fájlt, ha az adattitkosítást használja.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="e6cc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cc3-117">-DefaultProfile</span></span>
<span data-ttu-id="e6cc3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e6cc3-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e6cc3-119">-RecoveryPoint</span></span>
<span data-ttu-id="e6cc3-120">Azt a helyreállítási pont objektumot adja meg, amely megfelel az alkalmazni kívánt helyreállítási pontnak.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cc3-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6cc3-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e6cc3-122">Az ASR replikációs szolgáltatással védett elem objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-122">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cc3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cc3-123">-WhatIf</span></span>
<span data-ttu-id="e6cc3-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6cc3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6cc3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cc3-126">CommonParameters</span></span>
<span data-ttu-id="e6cc3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6cc3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cc3-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cc3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cc3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6cc3-129">INPUTS</span></span>

### <span data-ttu-id="e6cc3-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6cc3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e6cc3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6cc3-131">OUTPUTS</span></span>

### <span data-ttu-id="e6cc3-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e6cc3-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e6cc3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6cc3-133">NOTES</span></span>

## <span data-ttu-id="e6cc3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6cc3-134">RELATED LINKS</span></span>

[<span data-ttu-id="e6cc3-135">Azure webhely-helyreállítási parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e6cc3-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
