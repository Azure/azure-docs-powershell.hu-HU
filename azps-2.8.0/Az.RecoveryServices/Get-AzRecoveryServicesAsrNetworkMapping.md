---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 56b8f70494a8575c569aa7a2ee9636521f8a87ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838621"
---
# <span data-ttu-id="3234c-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3234c-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3234c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3234c-102">SYNOPSIS</span></span>
<span data-ttu-id="3234c-103">Információt kap a webhely-helyreállítási hálózati megfeleltetésekről az aktuális boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="3234c-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="3234c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3234c-104">SYNTAX</span></span>

### <span data-ttu-id="3234c-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3234c-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3234c-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="3234c-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3234c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3234c-107">DESCRIPTION</span></span>
<span data-ttu-id="3234c-108">A **Get-AzRecoveryServicesAsrNetworkMapping** parancsmag információt kap az Azure webhely-helyreállítási hálózati megfeleltetésekről a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="3234c-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="3234c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3234c-109">EXAMPLES</span></span>

### <span data-ttu-id="3234c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3234c-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="3234c-111">Az átadott hálózat minden hálózati megfeleltetésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="3234c-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="3234c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3234c-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="3234c-113">Beolvassa a hálózati megfeleltetést a megadott névvel a megadott Azure webhely-helyreállítási anyagban.</span><span class="sxs-lookup"><span data-stu-id="3234c-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="3234c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3234c-114">PARAMETERS</span></span>

### <span data-ttu-id="3234c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3234c-115">-DefaultProfile</span></span>
<span data-ttu-id="3234c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3234c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3234c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3234c-117">-Name</span></span>
<span data-ttu-id="3234c-118">A beszerzéshez használandó ASR-hálózati megfeleltetési objektum neve.</span><span class="sxs-lookup"><span data-stu-id="3234c-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="3234c-119">– Hálózat</span><span class="sxs-lookup"><span data-stu-id="3234c-119">-Network</span></span>
<span data-ttu-id="3234c-120">A megadott hálózati ASR-objektumnak megfelelő ASR-hálózati megfeleltetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3234c-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="3234c-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="3234c-121">-PrimaryFabric</span></span>
<span data-ttu-id="3234c-122">A megadott elsődleges szövet objektumhoz tartozó ASR-hálózati megfeleltetések beszerzése</span><span class="sxs-lookup"><span data-stu-id="3234c-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="3234c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3234c-123">CommonParameters</span></span>
<span data-ttu-id="3234c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3234c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3234c-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3234c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3234c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3234c-126">INPUTS</span></span>

### <span data-ttu-id="3234c-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="3234c-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="3234c-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3234c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3234c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3234c-129">OUTPUTS</span></span>

### <span data-ttu-id="3234c-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3234c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="3234c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3234c-131">NOTES</span></span>

## <span data-ttu-id="3234c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3234c-132">RELATED LINKS</span></span>

[<span data-ttu-id="3234c-133">Új – AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3234c-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3234c-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3234c-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
