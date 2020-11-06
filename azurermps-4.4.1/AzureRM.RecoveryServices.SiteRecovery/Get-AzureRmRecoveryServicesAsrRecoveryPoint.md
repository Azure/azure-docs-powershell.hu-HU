---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 96a30621bc545b635262fd7937e0e55739d0be7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504791"
---
# <span data-ttu-id="9ce5f-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9ce5f-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="9ce5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ce5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce5f-103">A replikációs védelemmel ellátott elemek számára elérhető helyreállítási pontok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="9ce5f-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ce5f-104">SYNTAX</span></span>

### <span data-ttu-id="9ce5f-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ce5f-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [<CommonParameters>]
```

### <span data-ttu-id="9ce5f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9ce5f-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [<CommonParameters>]
```

## <span data-ttu-id="9ce5f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ce5f-107">DESCRIPTION</span></span>
<span data-ttu-id="9ce5f-108">A **Get-AzureRmRecoveryServicesAsrRecoveryPoint** parancsmag a replikációs védelemmel ellátott elemek esetén elérhető helyreállítási pontok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ce5f-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="9ce5f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9ce5f-109">EXAMPLES</span></span>

### <span data-ttu-id="9ce5f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ce5f-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="9ce5f-111">A megadott ASR-replikációs védett elem helyreállítási pontjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="9ce5f-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="9ce5f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ce5f-112">PARAMETERS</span></span>

### <span data-ttu-id="9ce5f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ce5f-113">-Name</span></span>
<span data-ttu-id="9ce5f-114">A beolvasott helyreállítási pont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ce5f-114">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce5f-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9ce5f-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9ce5f-116">Itt adhatja meg az Azure webhely-helyreállítási replikációval védett elem objektumát, amelyhez az elérhető helyreállítási pontok listáját beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="9ce5f-116">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="9ce5f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce5f-117">CommonParameters</span></span>
<span data-ttu-id="9ce5f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ce5f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce5f-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ce5f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce5f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ce5f-120">INPUTS</span></span>

### <span data-ttu-id="9ce5f-121">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9ce5f-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9ce5f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ce5f-122">OUTPUTS</span></span>

### <span data-ttu-id="9ce5f-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9ce5f-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9ce5f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ce5f-124">NOTES</span></span>

## <span data-ttu-id="9ce5f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ce5f-125">RELATED LINKS</span></span>

[<span data-ttu-id="9ce5f-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ce5f-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9ce5f-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ce5f-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9ce5f-128">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ce5f-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9ce5f-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ce5f-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9ce5f-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ce5f-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
