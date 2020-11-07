---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: b381f611d47306c9327d1b276aa3773c34c7b3e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838607"
---
# <span data-ttu-id="4aadc-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4aadc-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="4aadc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4aadc-102">SYNOPSIS</span></span>
<span data-ttu-id="4aadc-103">A replikációs védelemmel ellátott elemek számára elérhető helyreállítási pontok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4aadc-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="4aadc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4aadc-104">SYNTAX</span></span>

### <span data-ttu-id="4aadc-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4aadc-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aadc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4aadc-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aadc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4aadc-107">DESCRIPTION</span></span>
<span data-ttu-id="4aadc-108">A **Get-AzRecoveryServicesAsrRecoveryPoint** parancsmag a replikációs védelemmel ellátott elemek esetén elérhető helyreállítási pontok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4aadc-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="4aadc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4aadc-109">EXAMPLES</span></span>

### <span data-ttu-id="4aadc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4aadc-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="4aadc-111">A megadott ASR-replikációs védett elem helyreállítási pontjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4aadc-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="4aadc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4aadc-112">PARAMETERS</span></span>

### <span data-ttu-id="4aadc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aadc-113">-DefaultProfile</span></span>
<span data-ttu-id="4aadc-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4aadc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4aadc-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4aadc-115">-Name</span></span>
<span data-ttu-id="4aadc-116">A beolvasott helyreállítási pont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4aadc-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="4aadc-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4aadc-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4aadc-118">Itt adhatja meg az Azure webhely-helyreállítási replikációval védett elem objektumát, amelyhez az elérhető helyreállítási pontok listáját beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="4aadc-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="4aadc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aadc-119">CommonParameters</span></span>
<span data-ttu-id="4aadc-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4aadc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aadc-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aadc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aadc-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aadc-122">INPUTS</span></span>

### <span data-ttu-id="4aadc-123">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4aadc-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4aadc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aadc-124">OUTPUTS</span></span>

### <span data-ttu-id="4aadc-125">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4aadc-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="4aadc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4aadc-126">NOTES</span></span>

## <span data-ttu-id="4aadc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4aadc-127">RELATED LINKS</span></span>

[<span data-ttu-id="4aadc-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4aadc-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4aadc-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4aadc-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4aadc-130">Új – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4aadc-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4aadc-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4aadc-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4aadc-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4aadc-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
