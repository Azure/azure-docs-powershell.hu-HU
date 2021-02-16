---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169298"
---
# <span data-ttu-id="7af4c-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="7af4c-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="7af4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7af4c-102">SYNOPSIS</span></span>
<span data-ttu-id="7af4c-103">Információkat kap a webhely-helyreállítás által kezelt hálózatokról az aktuális tárolóban.</span><span class="sxs-lookup"><span data-stu-id="7af4c-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="7af4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7af4c-104">SYNTAX</span></span>

### <span data-ttu-id="7af4c-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7af4c-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7af4c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7af4c-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7af4c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7af4c-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7af4c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7af4c-108">DESCRIPTION</span></span>
<span data-ttu-id="7af4c-109">A **Get-AzRecoveryServicesAsrNetwork** parancsmag információkat kap az Aktuális Azure-webhely-helyreállítási tároló Azure Webhely-helyreállítási hálózatairól.</span><span class="sxs-lookup"><span data-stu-id="7af4c-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7af4c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7af4c-110">EXAMPLES</span></span>

### <span data-ttu-id="7af4c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7af4c-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="7af4c-112">A megadott anyagban található összes ismert hálózatot beveszi.</span><span class="sxs-lookup"><span data-stu-id="7af4c-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="7af4c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7af4c-113">PARAMETERS</span></span>

### <span data-ttu-id="7af4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af4c-114">-DefaultProfile</span></span>
<span data-ttu-id="7af4c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7af4c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7af4c-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="7af4c-116">-Fabric</span></span>
<span data-ttu-id="7af4c-117">ASR fabric object</span><span class="sxs-lookup"><span data-stu-id="7af4c-117">ASR fabric object</span></span>

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

### <span data-ttu-id="7af4c-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7af4c-118">-FriendlyName</span></span>
<span data-ttu-id="7af4c-119">A hálózati ASR-objektum rövid neve.</span><span class="sxs-lookup"><span data-stu-id="7af4c-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="7af4c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7af4c-120">-Name</span></span>
<span data-ttu-id="7af4c-121">A hálózati ASR-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="7af4c-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="7af4c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af4c-122">CommonParameters</span></span>
<span data-ttu-id="7af4c-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af4c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af4c-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7af4c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af4c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7af4c-125">INPUTS</span></span>

### <span data-ttu-id="7af4c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7af4c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7af4c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7af4c-127">OUTPUTS</span></span>

### <span data-ttu-id="7af4c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="7af4c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="7af4c-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7af4c-129">NOTES</span></span>

## <span data-ttu-id="7af4c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7af4c-130">RELATED LINKS</span></span>
