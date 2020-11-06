---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494643"
---
# <span data-ttu-id="3fe7d-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3fe7d-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="3fe7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3fe7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe7d-103">A feladatátvételi művelet véglegesítése előtt módosítja a sikertelenül védett elem helyreállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fe7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3fe7d-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fe7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3fe7d-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe7d-106">A **kezdő AzureRmSiteRecoveryApplyRecoveryPoint** a sikertelenül védett elem helyreállítási pontját a feladatátvételi művelet véglegesítése előtt módosítja.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="3fe7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3fe7d-107">EXAMPLES</span></span>

## <span data-ttu-id="3fe7d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3fe7d-108">PARAMETERS</span></span>

### <span data-ttu-id="3fe7d-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="3fe7d-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="3fe7d-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="3fe7d-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="3fe7d-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3fe7d-111">-RecoveryPoint</span></span>
<span data-ttu-id="3fe7d-112">Annak a helyreállítási pont objektumnak a meghatározása, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe7d-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3fe7d-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3fe7d-114">A replikációs védelemmel ellátott elem objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-114">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe7d-115">-DefaultProfile</span></span>
<span data-ttu-id="3fe7d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fe7d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe7d-117">CommonParameters</span></span>
<span data-ttu-id="3fe7d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3fe7d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe7d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe7d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe7d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fe7d-120">INPUTS</span></span>

### <span data-ttu-id="3fe7d-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3fe7d-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="3fe7d-122">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3fe7d-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="3fe7d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fe7d-123">OUTPUTS</span></span>

### <span data-ttu-id="3fe7d-124">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3fe7d-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3fe7d-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3fe7d-125">NOTES</span></span>

## <span data-ttu-id="3fe7d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fe7d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3fe7d-127">Azure webhely-helyreállítási parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3fe7d-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
