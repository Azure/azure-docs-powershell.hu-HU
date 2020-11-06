---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 21a01ae07c383484a6ec8e17d9b09a93671bfbe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493978"
---
# <span data-ttu-id="df7c7-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="df7c7-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="df7c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="df7c7-103">A replikációs védelemmel ellátott elemek számára elérhető helyreállítási pontok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="df7c7-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df7c7-104">SYNTAX</span></span>

### <span data-ttu-id="df7c7-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df7c7-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df7c7-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="df7c7-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df7c7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df7c7-107">DESCRIPTION</span></span>
<span data-ttu-id="df7c7-108">A **Get-AzureRmRecoveryServicesAsrRecoveryPoint** parancsmag a replikációs védelemmel ellátott elemek esetén elérhető helyreállítási pontok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="df7c7-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="df7c7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df7c7-109">EXAMPLES</span></span>

### <span data-ttu-id="df7c7-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="df7c7-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="df7c7-111">A megadott ASR-replikációs védett elem helyreállítási pontjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="df7c7-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="df7c7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df7c7-112">PARAMETERS</span></span>

### <span data-ttu-id="df7c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7c7-113">-DefaultProfile</span></span>
<span data-ttu-id="df7c7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df7c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="df7c7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df7c7-115">-Name</span></span>
<span data-ttu-id="df7c7-116">A beolvasott helyreállítási pont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df7c7-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7c7-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="df7c7-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="df7c7-118">Itt adhatja meg az Azure webhely-helyreállítási replikációval védett elem objektumát, amelyhez az elérhető helyreállítási pontok listáját beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="df7c7-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="df7c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7c7-119">CommonParameters</span></span>
<span data-ttu-id="df7c7-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df7c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7c7-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7c7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7c7-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df7c7-122">INPUTS</span></span>

### <span data-ttu-id="df7c7-123">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="df7c7-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="df7c7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df7c7-124">OUTPUTS</span></span>

### <span data-ttu-id="df7c7-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="df7c7-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="df7c7-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df7c7-126">NOTES</span></span>

## <span data-ttu-id="df7c7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df7c7-127">RELATED LINKS</span></span>

[<span data-ttu-id="df7c7-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="df7c7-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="df7c7-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="df7c7-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="df7c7-130">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="df7c7-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="df7c7-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="df7c7-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="df7c7-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="df7c7-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
