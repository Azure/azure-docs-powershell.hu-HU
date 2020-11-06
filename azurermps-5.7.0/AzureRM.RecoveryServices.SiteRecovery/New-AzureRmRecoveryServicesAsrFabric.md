---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 53398a882ff513443f8eae336539858f7fe34ce4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498895"
---
# <span data-ttu-id="4a7eb-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4a7eb-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="4a7eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a7eb-103">Azure-webhely-helyreállítási szövetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a7eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a7eb-104">SYNTAX</span></span>

### <span data-ttu-id="4a7eb-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a7eb-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a7eb-106">Azure</span><span class="sxs-lookup"><span data-stu-id="4a7eb-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a7eb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a7eb-107">DESCRIPTION</span></span>
<span data-ttu-id="4a7eb-108">A **New-AzureRmRecoveryServicesAsrFabric** parancsmag a megadott típusú Azure webhely-helyreállítási szerkezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="4a7eb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4a7eb-109">EXAMPLES</span></span>

### <span data-ttu-id="4a7eb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4a7eb-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="4a7eb-111">Az átadott névvel elindítja a szerkezet-készítést, és visszaadja a kelme-létrehozási művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="4a7eb-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4a7eb-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="4a7eb-113">Elindítja az Azure Fabric-készítést az átadott névvel, és visszaadja a szerkezet létrehozásának műveletének nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="4a7eb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a7eb-114">PARAMETERS</span></span>

### <span data-ttu-id="4a7eb-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="4a7eb-115">-Azure</span></span>
<span data-ttu-id="4a7eb-116">A kapcsoló paraméter az Azure-szövet létrehozását jelzi.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-116">Switch parameter indicates creation of azure fabric.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a7eb-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a7eb-117">-Confirm</span></span>
<span data-ttu-id="4a7eb-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a7eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a7eb-119">-DefaultProfile</span></span>
<span data-ttu-id="4a7eb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="4a7eb-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="4a7eb-121">-Location</span></span>
<span data-ttu-id="4a7eb-122">A létrehozott anyag objektumnak megfelelő Azure-régiót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-122">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="4a7eb-123">Az Azure site Recovery Fabric objektum a régiót jelöli.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-123">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="4a7eb-124">Két Azure-régió közötti replikálást szolgáló virtuális gépek esetében az elsődleges anyag az elsődleges Azure-régió és a helyreállítási anyag.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-124">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a7eb-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a7eb-125">-Name</span></span>
<span data-ttu-id="4a7eb-126">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-126">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a7eb-127">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="4a7eb-127">-Type</span></span>
<span data-ttu-id="4a7eb-128">Az Azure webhely-helyreállítási anyag típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-128">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a7eb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a7eb-129">-WhatIf</span></span>
<span data-ttu-id="4a7eb-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a7eb-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a7eb-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a7eb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a7eb-132">CommonParameters</span></span>
<span data-ttu-id="4a7eb-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a7eb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a7eb-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a7eb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a7eb-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a7eb-135">INPUTS</span></span>

### <span data-ttu-id="4a7eb-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="4a7eb-136">None</span></span>

## <span data-ttu-id="4a7eb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a7eb-137">OUTPUTS</span></span>

### <span data-ttu-id="4a7eb-138">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4a7eb-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4a7eb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a7eb-139">NOTES</span></span>

## <span data-ttu-id="4a7eb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a7eb-140">RELATED LINKS</span></span>

[<span data-ttu-id="4a7eb-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4a7eb-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="4a7eb-142">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4a7eb-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
