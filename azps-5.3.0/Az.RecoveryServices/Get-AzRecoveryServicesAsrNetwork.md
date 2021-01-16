---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476769"
---
# <span data-ttu-id="f3f99-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="f3f99-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="f3f99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f99-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f99-103">Információkat kap a webhely-helyreállítás által kezelt hálózatokról az aktuális tárolóban.</span><span class="sxs-lookup"><span data-stu-id="f3f99-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="f3f99-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3f99-104">SYNTAX</span></span>

### <span data-ttu-id="f3f99-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3f99-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3f99-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f3f99-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3f99-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3f99-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f99-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3f99-108">DESCRIPTION</span></span>
<span data-ttu-id="f3f99-109">A **Get-AzRecoveryServicesAsrNetwork** parancsmag információkat kap az Aktuális Azure-webhely-helyreállítási tároló Azure Webhely-helyreállítási hálózatairól.</span><span class="sxs-lookup"><span data-stu-id="f3f99-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f3f99-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3f99-110">EXAMPLES</span></span>

### <span data-ttu-id="f3f99-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3f99-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="f3f99-112">A megadott anyagban található összes ismert hálózatot beveszi.</span><span class="sxs-lookup"><span data-stu-id="f3f99-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="f3f99-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3f99-113">PARAMETERS</span></span>

### <span data-ttu-id="f3f99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f99-114">-DefaultProfile</span></span>
<span data-ttu-id="f3f99-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3f99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f3f99-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="f3f99-116">-Fabric</span></span>
<span data-ttu-id="f3f99-117">ASR fabric object</span><span class="sxs-lookup"><span data-stu-id="f3f99-117">ASR fabric object</span></span>

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

### <span data-ttu-id="f3f99-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3f99-118">-FriendlyName</span></span>
<span data-ttu-id="f3f99-119">A hálózati ASR-objektum rövid neve.</span><span class="sxs-lookup"><span data-stu-id="f3f99-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="f3f99-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f3f99-120">-Name</span></span>
<span data-ttu-id="f3f99-121">A hálózati ASR-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="f3f99-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="f3f99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f99-122">CommonParameters</span></span>
<span data-ttu-id="f3f99-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f99-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3f99-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f99-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3f99-125">INPUTS</span></span>

### <span data-ttu-id="f3f99-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f3f99-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f3f99-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f99-127">OUTPUTS</span></span>

### <span data-ttu-id="f3f99-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="f3f99-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="f3f99-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3f99-129">NOTES</span></span>

## <span data-ttu-id="f3f99-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3f99-130">RELATED LINKS</span></span>
