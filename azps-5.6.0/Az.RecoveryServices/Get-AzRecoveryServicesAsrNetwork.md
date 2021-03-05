---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 54c90e4dac97084ed371e0f5f9011bbcef0a254e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003254"
---
# <span data-ttu-id="e8e3d-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="e8e3d-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="e8e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e3d-103">Információkat kap a webhely-helyreállítás által kezelt hálózatokról az aktuális tárolóban.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="e8e3d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e8e3d-104">SYNTAX</span></span>

### <span data-ttu-id="e8e3d-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8e3d-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e3d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e8e3d-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e3d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e8e3d-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8e3d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e8e3d-108">DESCRIPTION</span></span>
<span data-ttu-id="e8e3d-109">A **Get-AzRecoveryServicesAsrNetwork** parancsmag információkat kap az Aktuális Azure-webhely-helyreállítási tároló Azure Webhely-helyreállítási hálózatairól.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e8e3d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e8e3d-110">EXAMPLES</span></span>

### <span data-ttu-id="e8e3d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e8e3d-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="e8e3d-112">A megadott anyagban található összes ismert hálózatot beveszi.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="e8e3d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8e3d-113">PARAMETERS</span></span>

### <span data-ttu-id="e8e3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e3d-114">-DefaultProfile</span></span>
<span data-ttu-id="e8e3d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e8e3d-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e8e3d-116">-Fabric</span></span>
<span data-ttu-id="e8e3d-117">ASR fabric object</span><span class="sxs-lookup"><span data-stu-id="e8e3d-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e3d-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e8e3d-118">-FriendlyName</span></span>
<span data-ttu-id="e8e3d-119">A hálózati ASR-objektum rövid neve.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e3d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e8e3d-120">-Name</span></span>
<span data-ttu-id="e8e3d-121">A hálózati ASR-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="e8e3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e3d-122">CommonParameters</span></span>
<span data-ttu-id="e8e3d-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e3d-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8e3d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e3d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8e3d-125">INPUTS</span></span>

### <span data-ttu-id="e8e3d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e8e3d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e8e3d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8e3d-127">OUTPUTS</span></span>

### <span data-ttu-id="e8e3d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="e8e3d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="e8e3d-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e8e3d-129">NOTES</span></span>

## <span data-ttu-id="e8e3d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8e3d-130">RELATED LINKS</span></span>
