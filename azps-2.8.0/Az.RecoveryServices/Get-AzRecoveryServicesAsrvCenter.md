---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 48437526fdaf8ae226ff7693b417fcff7ffc93d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838599"
---
# <span data-ttu-id="6ced0-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="6ced0-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="6ced0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ced0-102">SYNOPSIS</span></span>
<span data-ttu-id="6ced0-103">Az ASR-szövet által megadott konfigurációs kiszolgálón a felderítéshez regisztrált vCenter-kiszolgálók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6ced0-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="6ced0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ced0-104">SYNTAX</span></span>

### <span data-ttu-id="6ced0-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ced0-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ced0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ced0-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ced0-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6ced0-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ced0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ced0-108">DESCRIPTION</span></span>
<span data-ttu-id="6ced0-109">A **Get-AzRecoveryServicesAsrvCenter** parancsmag részletesen ismerteti az ASR-anyag által megadott konfigurációs kiszolgálón a felderítéshez regisztrált vCenter-kiszolgálók adatait.</span><span class="sxs-lookup"><span data-stu-id="6ced0-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="6ced0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6ced0-110">EXAMPLES</span></span>

### <span data-ttu-id="6ced0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ced0-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="6ced0-112">Az Azure webhely-helyreállítási vCenter a szövet neve és a vCenter neve alapján érheti el.</span><span class="sxs-lookup"><span data-stu-id="6ced0-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="6ced0-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6ced0-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="6ced0-114">Az Azure webhely-helyreállítási vCenter listájának beszerzése szövet neve szerint</span><span class="sxs-lookup"><span data-stu-id="6ced0-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="6ced0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ced0-115">PARAMETERS</span></span>

### <span data-ttu-id="6ced0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ced0-116">-DefaultProfile</span></span>
<span data-ttu-id="6ced0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ced0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ced0-118">-Szövet</span><span class="sxs-lookup"><span data-stu-id="6ced0-118">-Fabric</span></span>
<span data-ttu-id="6ced0-119">A konfigurációs kiszolgálót jelképező ASR-anyag objektum.</span><span class="sxs-lookup"><span data-stu-id="6ced0-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="6ced0-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ced0-120">-Name</span></span>
<span data-ttu-id="6ced0-121">A vCenter-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6ced0-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="6ced0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ced0-122">-ResourceId</span></span>
<span data-ttu-id="6ced0-123">A vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ced0-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="6ced0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ced0-124">CommonParameters</span></span>
<span data-ttu-id="6ced0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ced0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ced0-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ced0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ced0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ced0-127">INPUTS</span></span>

### <span data-ttu-id="6ced0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6ced0-128">System.String</span></span>

### <span data-ttu-id="6ced0-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6ced0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6ced0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ced0-130">OUTPUTS</span></span>

### <span data-ttu-id="6ced0-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="6ced0-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="6ced0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ced0-132">NOTES</span></span>

## <span data-ttu-id="6ced0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ced0-133">RELATED LINKS</span></span>
