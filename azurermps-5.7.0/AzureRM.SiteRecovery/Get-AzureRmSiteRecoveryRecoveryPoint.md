---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 42a0a96a32bf1b7f556ee2787f43a5777afa1115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502403"
---
# <span data-ttu-id="51e88-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="51e88-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="51e88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51e88-102">SYNOPSIS</span></span>
<span data-ttu-id="51e88-103">Elérhető helyreállítási pontok jelennek meg a replikációs védelemmel ellátott elemek között.</span><span class="sxs-lookup"><span data-stu-id="51e88-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51e88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51e88-104">SYNTAX</span></span>

### <span data-ttu-id="51e88-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51e88-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51e88-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="51e88-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51e88-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="51e88-107">DESCRIPTION</span></span>
<span data-ttu-id="51e88-108">A **Get-AzureRmSiteRecoveryRecoveryPoint** parancsmag a replikációs védelemmel ellátott elemek esetén elérhető helyreállítási pontok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="51e88-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="51e88-109">Példák</span><span class="sxs-lookup"><span data-stu-id="51e88-109">EXAMPLES</span></span>

## <span data-ttu-id="51e88-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51e88-110">PARAMETERS</span></span>

### <span data-ttu-id="51e88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e88-111">-DefaultProfile</span></span>
<span data-ttu-id="51e88-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51e88-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51e88-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51e88-113">-Name</span></span>
<span data-ttu-id="51e88-114">Annak a helyreállítási pontnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="51e88-114">Specifies the name of the recovery point this cmdlet gets.</span></span>

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

### <span data-ttu-id="51e88-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="51e88-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="51e88-116">Az Azure site Recovery Replication Protected Item objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51e88-116">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

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

### <span data-ttu-id="51e88-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e88-117">CommonParameters</span></span>
<span data-ttu-id="51e88-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51e88-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e88-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e88-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e88-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51e88-120">INPUTS</span></span>

### <span data-ttu-id="51e88-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="51e88-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="51e88-122">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="51e88-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="51e88-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51e88-123">OUTPUTS</span></span>

### <span data-ttu-id="51e88-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="51e88-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="51e88-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51e88-125">NOTES</span></span>

## <span data-ttu-id="51e88-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51e88-126">RELATED LINKS</span></span>

[<span data-ttu-id="51e88-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="51e88-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="51e88-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="51e88-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="51e88-129">Új – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="51e88-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="51e88-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="51e88-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="51e88-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="51e88-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
