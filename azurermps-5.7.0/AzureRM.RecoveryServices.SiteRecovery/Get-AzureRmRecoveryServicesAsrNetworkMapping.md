---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 442fd62393b33cc69e8f5a38f726bb8816c5bc64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494416"
---
# <span data-ttu-id="bdd32-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bdd32-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="bdd32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdd32-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd32-103">Információt kap a webhely-helyreállítási hálózati megfeleltetésekről az aktuális boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="bdd32-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdd32-104">SYNTAX</span></span>

### <span data-ttu-id="bdd32-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdd32-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdd32-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="bdd32-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdd32-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdd32-107">DESCRIPTION</span></span>
<span data-ttu-id="bdd32-108">A **Get-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag információt kap az Azure webhely-helyreállítási hálózati megfeleltetésekről a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="bdd32-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="bdd32-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bdd32-109">EXAMPLES</span></span>

### <span data-ttu-id="bdd32-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bdd32-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="bdd32-111">Az átadott hálózat minden hálózati megfeleltetésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="bdd32-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="bdd32-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="bdd32-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="bdd32-113">Beolvassa a hálózati megfeleltetést a megadott névvel a megadott Azure webhely-helyreállítási anyagban.</span><span class="sxs-lookup"><span data-stu-id="bdd32-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="bdd32-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdd32-114">PARAMETERS</span></span>

### <span data-ttu-id="bdd32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd32-115">-DefaultProfile</span></span>
<span data-ttu-id="bdd32-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdd32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="bdd32-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bdd32-117">-Name</span></span>
<span data-ttu-id="bdd32-118">A beszerzéshez használandó ASR-hálózati megfeleltetési objektum neve.</span><span class="sxs-lookup"><span data-stu-id="bdd32-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd32-119">– Hálózat</span><span class="sxs-lookup"><span data-stu-id="bdd32-119">-Network</span></span>
<span data-ttu-id="bdd32-120">A megadott hálózati ASR-objektumnak megfelelő ASR-hálózati megfeleltetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="bdd32-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd32-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="bdd32-121">-PrimaryFabric</span></span>
<span data-ttu-id="bdd32-122">A megadott elsődleges szövet objektumhoz tartozó ASR-hálózati megfeleltetések beszerzése</span><span class="sxs-lookup"><span data-stu-id="bdd32-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd32-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd32-123">CommonParameters</span></span>
<span data-ttu-id="bdd32-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdd32-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd32-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd32-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd32-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd32-126">INPUTS</span></span>

### <span data-ttu-id="bdd32-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bdd32-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bdd32-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd32-128">OUTPUTS</span></span>

### <span data-ttu-id="bdd32-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bdd32-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bdd32-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdd32-130">NOTES</span></span>

## <span data-ttu-id="bdd32-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdd32-131">RELATED LINKS</span></span>

[<span data-ttu-id="bdd32-132">Új – AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bdd32-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="bdd32-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bdd32-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
