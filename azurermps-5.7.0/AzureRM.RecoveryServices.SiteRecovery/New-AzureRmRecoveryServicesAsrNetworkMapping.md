---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498892"
---
# <span data-ttu-id="00e8c-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00e8c-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="00e8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="00e8c-103">ASR-hálózati megfeleltetést hoz létre két hálózat között.</span><span class="sxs-lookup"><span data-stu-id="00e8c-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00e8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00e8c-104">SYNTAX</span></span>

### <span data-ttu-id="00e8c-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00e8c-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00e8c-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="00e8c-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e8c-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="00e8c-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00e8c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="00e8c-108">DESCRIPTION</span></span>
<span data-ttu-id="00e8c-109">A **New-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag a két hálózat közötti ASR-hálózati megfeleltetések létrehozásának működését indítja el, és a művelet nyomon követéséhez használt ASR-feladat értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="00e8c-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="00e8c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="00e8c-110">EXAMPLES</span></span>

### <span data-ttu-id="00e8c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00e8c-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="00e8c-112">A megadott név, elsődleges és helyreállítási hálózat segítségével elindítja a hálózati megfeleltetés létrehozásának műveletét, és egy ASR-feladatot ad eredményül a művelet nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="00e8c-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="00e8c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="00e8c-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="00e8c-114">A megadott név, elsődleges és helyreállítási hálózat segítségével elindítja a létrehozáshoz szükséges hálózati megfeleltetést, és egy ASR-feladatot ad eredményül a művelet nyomon követéséhez (Azure – Azure eset).</span><span class="sxs-lookup"><span data-stu-id="00e8c-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="00e8c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00e8c-115">PARAMETERS</span></span>

### <span data-ttu-id="00e8c-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="00e8c-116">-AzureToAzure</span></span>
<span data-ttu-id="00e8c-117">Kapcsoló paraméter, amely azt adja meg, hogy a létrehozott hálózati megfeleltetés a két Azure-régió között a replikált Azure Virtual Machines rendszerhez lesz használható.</span><span class="sxs-lookup"><span data-stu-id="00e8c-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00e8c-118">-Confirm</span></span>
<span data-ttu-id="00e8c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00e8c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00e8c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e8c-120">-DefaultProfile</span></span>
<span data-ttu-id="00e8c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00e8c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="00e8c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="00e8c-122">-Name</span></span>
<span data-ttu-id="00e8c-123">A létrehozandó ASR-hálózati megfeleltetés neve.</span><span class="sxs-lookup"><span data-stu-id="00e8c-123">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="00e8c-124">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="00e8c-124">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="00e8c-125">A megfeleltetés elsődleges hálózatának Azure virtuális hálózati AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="00e8c-125">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="00e8c-126">-PrimaryFabric</span></span>
<span data-ttu-id="00e8c-127">Specifes az ASR-anyagra, ahol a megfeleltetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="00e8c-127">Specifes the ASR fabric where mapping should be created.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-128">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="00e8c-128">-PrimaryNetwork</span></span>
<span data-ttu-id="00e8c-129">Az ASR-hálózat megfeleltetésének elsődleges hálózati objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00e8c-129">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-130">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="00e8c-130">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="00e8c-131">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="00e8c-131">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-132">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="00e8c-132">-RecoveryFabric</span></span>
<span data-ttu-id="00e8c-133">Az Azure site Recovery Fabric objektum a helyreállítási Azure-területnek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="00e8c-133">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-134">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="00e8c-134">-RecoveryNetwork</span></span>
<span data-ttu-id="00e8c-135">Az ASR-hálózati megfeleltetés helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00e8c-135">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00e8c-136">-WhatIf</span></span>
<span data-ttu-id="00e8c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00e8c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00e8c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00e8c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00e8c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e8c-139">CommonParameters</span></span>
<span data-ttu-id="00e8c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00e8c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e8c-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e8c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e8c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00e8c-142">INPUTS</span></span>

### <span data-ttu-id="00e8c-143">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="00e8c-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="00e8c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00e8c-144">OUTPUTS</span></span>

### <span data-ttu-id="00e8c-145">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="00e8c-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="00e8c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00e8c-146">NOTES</span></span>

## <span data-ttu-id="00e8c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00e8c-147">RELATED LINKS</span></span>

[<span data-ttu-id="00e8c-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00e8c-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="00e8c-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00e8c-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
