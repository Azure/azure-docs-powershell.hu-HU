---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 294af442998a49800f866ce1681365eae547ffd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669603"
---
# <span data-ttu-id="14601-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="14601-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="14601-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14601-102">SYNOPSIS</span></span>
<span data-ttu-id="14601-103">A feladatátvételi művelet véglegesítése előtt módosítja a sikertelenül védett elem helyreállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="14601-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

## <span data-ttu-id="14601-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14601-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14601-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14601-105">DESCRIPTION</span></span>
<span data-ttu-id="14601-106">A **kezdő AzRecoveryServicesAsrApplyRecoveryPoint** a sikertelenül védett elem helyreállítási pontját a feladatátvételi művelet véglegesítése előtt módosítja.</span><span class="sxs-lookup"><span data-stu-id="14601-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="14601-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14601-107">EXAMPLES</span></span>

### <span data-ttu-id="14601-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="14601-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="14601-109">A megadott helyreállítási pont alkalmazása a replikációs védelemmel ellátott elemre, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="14601-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="14601-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14601-110">PARAMETERS</span></span>

### <span data-ttu-id="14601-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="14601-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="14601-112">Az elsődleges tanúsítványfájl megadása, ha az adattitkosítást használják.</span><span class="sxs-lookup"><span data-stu-id="14601-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="14601-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="14601-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="14601-114">Megadja a másodlagos tanúsítványfájl-fájlt, ha az adattitkosítást használja.</span><span class="sxs-lookup"><span data-stu-id="14601-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="14601-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14601-115">-DefaultProfile</span></span>
<span data-ttu-id="14601-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14601-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="14601-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="14601-117">-RecoveryPoint</span></span>
<span data-ttu-id="14601-118">Azt a helyreállítási pont objektumot adja meg, amely megfelel az alkalmazni kívánt helyreállítási pontnak.</span><span class="sxs-lookup"><span data-stu-id="14601-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14601-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="14601-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="14601-120">Az ASR replikációs szolgáltatással védett elem objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="14601-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14601-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14601-121">-Confirm</span></span>
<span data-ttu-id="14601-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14601-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14601-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14601-123">-WhatIf</span></span>
<span data-ttu-id="14601-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14601-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14601-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14601-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14601-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14601-126">CommonParameters</span></span>
<span data-ttu-id="14601-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14601-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14601-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14601-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14601-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14601-129">INPUTS</span></span>

### <span data-ttu-id="14601-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="14601-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="14601-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14601-131">OUTPUTS</span></span>

### <span data-ttu-id="14601-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="14601-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="14601-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14601-133">NOTES</span></span>

## <span data-ttu-id="14601-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14601-134">RELATED LINKS</span></span>

[<span data-ttu-id="14601-135">Azure webhely-helyreállítási parancsmagok</span><span class="sxs-lookup"><span data-stu-id="14601-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
