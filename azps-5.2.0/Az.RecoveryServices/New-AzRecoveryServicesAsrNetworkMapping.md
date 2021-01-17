---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343073"
---
# <span data-ttu-id="6b393-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6b393-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="6b393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b393-102">SYNOPSIS</span></span>
<span data-ttu-id="6b393-103">AsR-hálózatleképezést hoz létre két hálózat között.</span><span class="sxs-lookup"><span data-stu-id="6b393-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="6b393-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b393-104">SYNTAX</span></span>

### <span data-ttu-id="6b393-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b393-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b393-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6b393-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b393-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6b393-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b393-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b393-108">DESCRIPTION</span></span>
<span data-ttu-id="6b393-109">A **New-AzRecoveryServicesAsrNetworkMapping** parancsmag elindítja két hálózat ASR-hálózatleképezésének létrehozását, és visszaadja a művelet nyomon követéséhez használt ASR-feladat ASR-feladatobjektumát.</span><span class="sxs-lookup"><span data-stu-id="6b393-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6b393-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b393-110">EXAMPLES</span></span>

### <span data-ttu-id="6b393-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b393-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="6b393-112">Elindítja a hálózatleképezés-létrehozási műveletet a megadott néven, elsődleges és helyreállítási hálózatokkal, és egy ASR-feladatot ad vissza a művelet nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="6b393-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="6b393-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6b393-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="6b393-114">Elindítja a létrehozási művelet hálózati megfeleltetését a megadott névvel, elsődleges és helyreállítási hálózatokkal, és egy ASR-feladatot ad vissza a művelet nyomon követéséhez (Azure–Azure eset).</span><span class="sxs-lookup"><span data-stu-id="6b393-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="6b393-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b393-115">PARAMETERS</span></span>

### <span data-ttu-id="6b393-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6b393-116">-AzureToAzure</span></span>
<span data-ttu-id="6b393-117">Flag to create AzureToAzure scenario.</span><span class="sxs-lookup"><span data-stu-id="6b393-117">Flag to create AzureToAzure scenario.</span></span>

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

### <span data-ttu-id="6b393-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b393-118">-DefaultProfile</span></span>
<span data-ttu-id="6b393-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b393-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b393-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6b393-120">-Name</span></span>
<span data-ttu-id="6b393-121">A létrehozni szükséges ASR-hálózatleképezés neve.</span><span class="sxs-lookup"><span data-stu-id="6b393-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="6b393-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6b393-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="6b393-123">A megfeleltetés elsődleges hálózatának Azure virtuális hálózatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b393-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="6b393-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="6b393-124">-PrimaryFabric</span></span>
<span data-ttu-id="6b393-125">Megadja azt az ASR-szövetet, amelyben megfeleltetést kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="6b393-125">Specifies the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="6b393-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="6b393-126">-PrimaryNetwork</span></span>
<span data-ttu-id="6b393-127">Az ASR-hálózatleképezés elsődleges hálózati objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b393-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="6b393-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6b393-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="6b393-129">A hálózati megfeleltetés helyreállítási Azure-hálózatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b393-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="6b393-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6b393-130">-RecoveryFabric</span></span>
<span data-ttu-id="6b393-131">A helyreállítási Azure-régiónak megfelelő Azure-webhely-helyreállítási hálóobjektum.</span><span class="sxs-lookup"><span data-stu-id="6b393-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="6b393-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6b393-132">-RecoveryNetwork</span></span>
<span data-ttu-id="6b393-133">Az ASR-hálózat megfeleltetésének helyreállítási hálózati objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b393-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="6b393-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b393-134">-Confirm</span></span>
<span data-ttu-id="6b393-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b393-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b393-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b393-136">-WhatIf</span></span>
<span data-ttu-id="6b393-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b393-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b393-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b393-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b393-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b393-139">CommonParameters</span></span>
<span data-ttu-id="6b393-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b393-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b393-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b393-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b393-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b393-142">INPUTS</span></span>

### <span data-ttu-id="6b393-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="6b393-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="6b393-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b393-144">OUTPUTS</span></span>

### <span data-ttu-id="6b393-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="6b393-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6b393-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b393-146">NOTES</span></span>

## <span data-ttu-id="6b393-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b393-147">RELATED LINKS</span></span>

[<span data-ttu-id="6b393-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6b393-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="6b393-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6b393-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
