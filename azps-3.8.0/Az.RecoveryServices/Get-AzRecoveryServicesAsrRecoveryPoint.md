---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010609"
---
# <span data-ttu-id="d97ab-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d97ab-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="d97ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d97ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d97ab-103">A replikációs védelemmel ellátott elemek számára elérhető helyreállítási pontok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d97ab-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="d97ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d97ab-104">SYNTAX</span></span>

### <span data-ttu-id="d97ab-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d97ab-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d97ab-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d97ab-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d97ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d97ab-107">DESCRIPTION</span></span>
<span data-ttu-id="d97ab-108">A **Get-AzRecoveryServicesAsrRecoveryPoint** parancsmag a replikációs védelemmel ellátott elemek esetén elérhető helyreállítási pontok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d97ab-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="d97ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d97ab-109">EXAMPLES</span></span>

### <span data-ttu-id="d97ab-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d97ab-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="d97ab-111">A megadott ASR-replikációs védett elem helyreállítási pontjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d97ab-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="d97ab-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d97ab-112">PARAMETERS</span></span>

### <span data-ttu-id="d97ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97ab-113">-DefaultProfile</span></span>
<span data-ttu-id="d97ab-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d97ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d97ab-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d97ab-115">-Name</span></span>
<span data-ttu-id="d97ab-116">A beolvasott helyreállítási pont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d97ab-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="d97ab-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d97ab-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d97ab-118">Itt adhatja meg az Azure webhely-helyreállítási replikációval védett elem objektumát, amelyhez az elérhető helyreállítási pontok listáját beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="d97ab-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="d97ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97ab-119">CommonParameters</span></span>
<span data-ttu-id="d97ab-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d97ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97ab-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d97ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97ab-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d97ab-122">INPUTS</span></span>

### <span data-ttu-id="d97ab-123">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d97ab-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d97ab-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d97ab-124">OUTPUTS</span></span>

### <span data-ttu-id="d97ab-125">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d97ab-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="d97ab-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d97ab-126">NOTES</span></span>

## <span data-ttu-id="d97ab-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d97ab-127">RELATED LINKS</span></span>

[<span data-ttu-id="d97ab-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d97ab-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d97ab-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d97ab-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d97ab-130">Új – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d97ab-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d97ab-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d97ab-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d97ab-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d97ab-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
