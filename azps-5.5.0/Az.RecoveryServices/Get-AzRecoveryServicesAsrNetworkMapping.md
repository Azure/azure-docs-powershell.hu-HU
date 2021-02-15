---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160267"
---
# <span data-ttu-id="1ebea-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1ebea-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="1ebea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ebea-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebea-103">Információkat kap a webhely-helyreállítási hálózat megfeleltetéseiről az aktuális tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="1ebea-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="1ebea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ebea-104">SYNTAX</span></span>

### <span data-ttu-id="1ebea-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ebea-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ebea-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="1ebea-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ebea-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ebea-107">DESCRIPTION</span></span>
<span data-ttu-id="1ebea-108">A **Get-AzRecoveryServicesAsrNetworkMapping** parancsmag információt kap a Helyreállítási szolgáltatások tároló Azure Site Recovery hálózati megfeleltetéseiről.</span><span class="sxs-lookup"><span data-stu-id="1ebea-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="1ebea-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ebea-109">EXAMPLES</span></span>

### <span data-ttu-id="1ebea-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ebea-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="1ebea-111">Az átadott hálózat összes hálózatleképezését beveszi.</span><span class="sxs-lookup"><span data-stu-id="1ebea-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="1ebea-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1ebea-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="1ebea-113">A megadott nevű hálózatok megfeleltetését kapja a megadott Azure-webhely-helyreállítási anyagban.</span><span class="sxs-lookup"><span data-stu-id="1ebea-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="1ebea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ebea-114">PARAMETERS</span></span>

### <span data-ttu-id="1ebea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebea-115">-DefaultProfile</span></span>
<span data-ttu-id="1ebea-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ebea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1ebea-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1ebea-117">-Name</span></span>
<span data-ttu-id="1ebea-118">A lekért ASR-hálózatleképezés-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="1ebea-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebea-119">-Network</span><span class="sxs-lookup"><span data-stu-id="1ebea-119">-Network</span></span>
<span data-ttu-id="1ebea-120">A megadott hálózati ASR-objektumnak megfelelő ASR-hálózati megfeleltetések lekérte.</span><span class="sxs-lookup"><span data-stu-id="1ebea-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ebea-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1ebea-121">-PrimaryFabric</span></span>
<span data-ttu-id="1ebea-122">Szerezze be a megadott elsődleges szövetobjektumnak megfelelő ASR-hálózati megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="1ebea-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ebea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebea-123">CommonParameters</span></span>
<span data-ttu-id="1ebea-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebea-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ebea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebea-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ebea-126">INPUTS</span></span>

### <span data-ttu-id="1ebea-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="1ebea-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="1ebea-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="1ebea-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="1ebea-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ebea-129">OUTPUTS</span></span>

### <span data-ttu-id="1ebea-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1ebea-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="1ebea-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ebea-131">NOTES</span></span>

## <span data-ttu-id="1ebea-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ebea-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ebea-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1ebea-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="1ebea-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1ebea-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
