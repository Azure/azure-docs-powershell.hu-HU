---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186023"
---
# <span data-ttu-id="6f3b7-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="6f3b7-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="6f3b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f3b7-103">Az ASR-szövet által megadott konfigurációs kiszolgálón a felderítéshez regisztrált vCenter-kiszolgálók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="6f3b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f3b7-104">SYNTAX</span></span>

### <span data-ttu-id="6f3b7-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f3b7-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f3b7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f3b7-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f3b7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6f3b7-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f3b7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f3b7-108">DESCRIPTION</span></span>
<span data-ttu-id="6f3b7-109">A **Get-AzRecoveryServicesAsrvCenter** parancsmag részletesen ismerteti az ASR-anyag által megadott konfigurációs kiszolgálón a felderítéshez regisztrált vCenter-kiszolgálók adatait.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="6f3b7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6f3b7-110">EXAMPLES</span></span>

### <span data-ttu-id="6f3b7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6f3b7-111">Example 1</span></span>
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

<span data-ttu-id="6f3b7-112">Az Azure webhely-helyreállítási vCenter a szövet neve és a vCenter neve alapján érheti el.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="6f3b7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6f3b7-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="6f3b7-114">Az Azure webhely-helyreállítási vCenter listájának beszerzése szövet neve szerint</span><span class="sxs-lookup"><span data-stu-id="6f3b7-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="6f3b7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f3b7-115">PARAMETERS</span></span>

### <span data-ttu-id="6f3b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f3b7-116">-DefaultProfile</span></span>
<span data-ttu-id="6f3b7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f3b7-118">-Szövet</span><span class="sxs-lookup"><span data-stu-id="6f3b7-118">-Fabric</span></span>
<span data-ttu-id="6f3b7-119">A konfigurációs kiszolgálót jelképező ASR-anyag objektum.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="6f3b7-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f3b7-120">-Name</span></span>
<span data-ttu-id="6f3b7-121">A vCenter-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="6f3b7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f3b7-122">-ResourceId</span></span>
<span data-ttu-id="6f3b7-123">A vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="6f3b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f3b7-124">CommonParameters</span></span>
<span data-ttu-id="6f3b7-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f3b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f3b7-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f3b7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f3b7-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f3b7-127">INPUTS</span></span>

### <span data-ttu-id="6f3b7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6f3b7-128">System.String</span></span>

### <span data-ttu-id="6f3b7-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6f3b7-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6f3b7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f3b7-130">OUTPUTS</span></span>

### <span data-ttu-id="6f3b7-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="6f3b7-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="6f3b7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f3b7-132">NOTES</span></span>

## <span data-ttu-id="6f3b7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f3b7-133">RELATED LINKS</span></span>