---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 8db3dd9579e528110ec41f59b1c29da5d132d18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502924"
---
# <span data-ttu-id="e8a02-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="e8a02-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="e8a02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8a02-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a02-103">Az ASR-szövet által megadott konfigurációs kiszolgálón a felderítéshez regisztrált vCenter-kiszolgálók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e8a02-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8a02-104">SYNTAX</span></span>

### <span data-ttu-id="e8a02-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8a02-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8a02-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8a02-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8a02-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e8a02-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a02-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8a02-108">DESCRIPTION</span></span>
<span data-ttu-id="e8a02-109">A **Get-AzureRmRecoveryServicesAsrvCenter** parancsmag részletesen ismerteti az ASR-anyag által megadott konfigurációs kiszolgálón a felderítéshez regisztrált vCenter-kiszolgálók adatait.</span><span class="sxs-lookup"><span data-stu-id="e8a02-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="e8a02-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e8a02-110">EXAMPLES</span></span>

### <span data-ttu-id="e8a02-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8a02-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="e8a02-112">Az Azure webhely-helyreállítási vCenter a szövet neve és a vCenter neve alapján érheti el.</span><span class="sxs-lookup"><span data-stu-id="e8a02-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="e8a02-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e8a02-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="e8a02-114">Az Azure webhely-helyreállítási vCenter listájának beszerzése szövet neve szerint</span><span class="sxs-lookup"><span data-stu-id="e8a02-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="e8a02-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8a02-115">PARAMETERS</span></span>

### <span data-ttu-id="e8a02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a02-116">-DefaultProfile</span></span>
<span data-ttu-id="e8a02-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8a02-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8a02-118">-Szövet</span><span class="sxs-lookup"><span data-stu-id="e8a02-118">-Fabric</span></span>
<span data-ttu-id="e8a02-119">A konfigurációs kiszolgálót jelképező ASR-anyag objektum.</span><span class="sxs-lookup"><span data-stu-id="e8a02-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a02-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8a02-120">-Name</span></span>
<span data-ttu-id="e8a02-121">A vCenter-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e8a02-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a02-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8a02-122">-ResourceId</span></span>
<span data-ttu-id="e8a02-123">A vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8a02-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a02-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a02-124">CommonParameters</span></span>
<span data-ttu-id="e8a02-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8a02-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a02-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8a02-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a02-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8a02-127">INPUTS</span></span>

### <span data-ttu-id="e8a02-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e8a02-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e8a02-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8a02-129">OUTPUTS</span></span>

### <span data-ttu-id="e8a02-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e8a02-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e8a02-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8a02-131">NOTES</span></span>

## <span data-ttu-id="e8a02-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8a02-132">RELATED LINKS</span></span>
