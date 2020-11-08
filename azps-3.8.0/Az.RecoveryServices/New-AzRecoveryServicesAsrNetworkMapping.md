---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014699"
---
# <span data-ttu-id="d7e55-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d7e55-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="d7e55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7e55-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e55-103">ASR-hálózati megfeleltetést hoz létre két hálózat között.</span><span class="sxs-lookup"><span data-stu-id="d7e55-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="d7e55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7e55-104">SYNTAX</span></span>

### <span data-ttu-id="d7e55-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7e55-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7e55-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d7e55-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7e55-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d7e55-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7e55-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7e55-108">DESCRIPTION</span></span>
<span data-ttu-id="d7e55-109">A **New-AzRecoveryServicesAsrNetworkMapping** parancsmag a két hálózat közötti ASR-hálózati megfeleltetések létrehozásának működését indítja el, és a művelet nyomon követéséhez használt ASR-feladat értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d7e55-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d7e55-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d7e55-110">EXAMPLES</span></span>

### <span data-ttu-id="d7e55-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d7e55-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="d7e55-112">A megadott név, elsődleges és helyreállítási hálózat segítségével elindítja a hálózati megfeleltetés létrehozásának műveletét, és egy ASR-feladatot ad eredményül a művelet nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d7e55-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="d7e55-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d7e55-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="d7e55-114">A megadott név, elsődleges és helyreállítási hálózat segítségével elindítja a létrehozáshoz szükséges hálózati megfeleltetést, és egy ASR-feladatot ad eredményül a művelet nyomon követéséhez (Azure – Azure eset).</span><span class="sxs-lookup"><span data-stu-id="d7e55-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="d7e55-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7e55-115">PARAMETERS</span></span>

### <span data-ttu-id="d7e55-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d7e55-116">-AzureToAzure</span></span>
<span data-ttu-id="d7e55-117">Jelölő: AzureToAzure-forgatókönyv létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d7e55-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e55-118">-DefaultProfile</span></span>
<span data-ttu-id="d7e55-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7e55-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d7e55-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7e55-120">-Name</span></span>
<span data-ttu-id="d7e55-121">A létrehozandó ASR-hálózati megfeleltetés neve.</span><span class="sxs-lookup"><span data-stu-id="d7e55-121">Name of the ASR network mapping to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="d7e55-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="d7e55-123">A megfeleltetés elsődleges hálózatának Azure virtuális hálózati AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e55-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="d7e55-124">-PrimaryFabric</span></span>
<span data-ttu-id="d7e55-125">Megadja az ASR-hálót, ahol a megfeleltetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="d7e55-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="d7e55-126">-PrimaryNetwork</span></span>
<span data-ttu-id="d7e55-127">Az ASR-hálózat megfeleltetésének elsődleges hálózati objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e55-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="d7e55-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="d7e55-129">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="d7e55-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d7e55-130">-RecoveryFabric</span></span>
<span data-ttu-id="d7e55-131">Az Azure site Recovery Fabric objektum a helyreállítási Azure-területnek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="d7e55-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d7e55-132">-RecoveryNetwork</span></span>
<span data-ttu-id="d7e55-133">Az ASR-hálózati megfeleltetés helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e55-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7e55-134">-Confirm</span></span>
<span data-ttu-id="d7e55-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7e55-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e55-136">-WhatIf</span></span>
<span data-ttu-id="d7e55-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7e55-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7e55-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7e55-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e55-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e55-139">CommonParameters</span></span>
<span data-ttu-id="d7e55-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7e55-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e55-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7e55-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e55-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e55-142">INPUTS</span></span>

### <span data-ttu-id="d7e55-143">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="d7e55-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="d7e55-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e55-144">OUTPUTS</span></span>

### <span data-ttu-id="d7e55-145">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d7e55-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d7e55-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7e55-146">NOTES</span></span>

## <span data-ttu-id="d7e55-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7e55-147">RELATED LINKS</span></span>

[<span data-ttu-id="d7e55-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d7e55-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="d7e55-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d7e55-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
