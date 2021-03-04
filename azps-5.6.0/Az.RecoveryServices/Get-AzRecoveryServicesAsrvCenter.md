---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: eb358a0caf2b1ea5ccba8d92c39562d2c39706c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941042"
---
# <span data-ttu-id="ec947-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="ec947-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="ec947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec947-102">SYNOPSIS</span></span>
<span data-ttu-id="ec947-103">Az ASR-anyag által meghatározott konfigurációs kiszolgálón felderítésre regisztrált vCenter-kiszolgálók részletei.</span><span class="sxs-lookup"><span data-stu-id="ec947-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="ec947-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec947-104">SYNTAX</span></span>

### <span data-ttu-id="ec947-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec947-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec947-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec947-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec947-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ec947-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec947-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec947-108">DESCRIPTION</span></span>
<span data-ttu-id="ec947-109">A **Get-AzRecoveryServicesAsrvCenter** parancsmag az ASR-anyag által meghatározott konfigurációs kiszolgálón feltárásra regisztrált vCenter-kiszolgálók adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ec947-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="ec947-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec947-110">EXAMPLES</span></span>

### <span data-ttu-id="ec947-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ec947-111">Example 1</span></span>
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

<span data-ttu-id="ec947-112">Szerezze be az Azure Site Recovery vCenter webhelyet a vCenter neve és anyaga alapján.</span><span class="sxs-lookup"><span data-stu-id="ec947-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="ec947-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ec947-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="ec947-114">Az Azure-webhely helyreállítási vCenter-listájának leszerzése anyagnév alapján.</span><span class="sxs-lookup"><span data-stu-id="ec947-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="ec947-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec947-115">PARAMETERS</span></span>

### <span data-ttu-id="ec947-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec947-116">-DefaultProfile</span></span>
<span data-ttu-id="ec947-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec947-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec947-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="ec947-118">-Fabric</span></span>
<span data-ttu-id="ec947-119">A Configuration Servert képviselő ASR-anyagobjektum.</span><span class="sxs-lookup"><span data-stu-id="ec947-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="ec947-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ec947-120">-Name</span></span>
<span data-ttu-id="ec947-121">A vCenter-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ec947-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="ec947-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec947-122">-ResourceId</span></span>
<span data-ttu-id="ec947-123">A vCenter erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec947-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="ec947-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec947-124">CommonParameters</span></span>
<span data-ttu-id="ec947-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec947-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec947-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec947-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec947-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec947-127">INPUTS</span></span>

### <span data-ttu-id="ec947-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ec947-128">System.String</span></span>

### <span data-ttu-id="ec947-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ec947-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ec947-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec947-130">OUTPUTS</span></span>

### <span data-ttu-id="ec947-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="ec947-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="ec947-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec947-132">NOTES</span></span>

## <span data-ttu-id="ec947-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec947-133">RELATED LINKS</span></span>
