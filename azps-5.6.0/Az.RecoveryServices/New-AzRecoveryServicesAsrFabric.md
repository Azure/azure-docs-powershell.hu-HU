---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: bfea43fb0f27aff6405159c0174a698d9dc2298e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003141"
---
# <span data-ttu-id="5c3e3-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5c3e3-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="5c3e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c3e3-103">Azure-webhely helyreállítási hálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="5c3e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c3e3-104">SYNTAX</span></span>

### <span data-ttu-id="5c3e3-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c3e3-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c3e3-106">Azure</span><span class="sxs-lookup"><span data-stu-id="5c3e3-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c3e3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c3e3-107">DESCRIPTION</span></span>
<span data-ttu-id="5c3e3-108">A **New-AzRecoveryServicesAsrFabric** parancsmag létrehoz egy megadott típusú Azure Site Recovery Fabricot.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="5c3e3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c3e3-109">EXAMPLES</span></span>

### <span data-ttu-id="5c3e3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5c3e3-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="5c3e3-111">A szövetkészítést a megfelelő névvel kezdi, és visszaadja a szövetkészítés nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="5c3e3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="5c3e3-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="5c3e3-113">Az Azure Fabric létrehozását a megfelelő névvel kezdi, és visszaadja a szövetkészítési művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="5c3e3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c3e3-114">PARAMETERS</span></span>

### <span data-ttu-id="5c3e3-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="5c3e3-115">-Azure</span></span>
<span data-ttu-id="5c3e3-116">A Kapcsoló paraméter az Azure-anyag létrehozásához ad meg egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c3e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c3e3-117">-DefaultProfile</span></span>
<span data-ttu-id="5c3e3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5c3e3-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5c3e3-119">-Location</span></span>
<span data-ttu-id="5c3e3-120">A létrehozott Fabric objektumnak megfelelő Azure-régiót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="5c3e3-121">Az Azure Site Recovery szövetobjektum egy régiót képvisel.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="5c3e3-122">A két Azure-régió között replikált virtuális gépek esetében egy elsődleges szövet képviseli az elsődleges Azure-régiót és a helyreállítási szerkezetet.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c3e3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5c3e3-123">-Name</span></span>
<span data-ttu-id="5c3e3-124">Az Azure Site Recovery Fabric nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="5c3e3-125">-Type</span><span class="sxs-lookup"><span data-stu-id="5c3e3-125">-Type</span></span>
<span data-ttu-id="5c3e3-126">Az Azure Site Recovery Fabric típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c3e3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c3e3-127">-Confirm</span></span>
<span data-ttu-id="5c3e3-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c3e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c3e3-129">-WhatIf</span></span>
<span data-ttu-id="5c3e3-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c3e3-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c3e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c3e3-132">CommonParameters</span></span>
<span data-ttu-id="5c3e3-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c3e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c3e3-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c3e3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c3e3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c3e3-135">INPUTS</span></span>

### <span data-ttu-id="5c3e3-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="5c3e3-136">None</span></span>

## <span data-ttu-id="5c3e3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c3e3-137">OUTPUTS</span></span>

### <span data-ttu-id="5c3e3-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="5c3e3-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c3e3-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c3e3-139">NOTES</span></span>

## <span data-ttu-id="5c3e3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c3e3-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c3e3-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5c3e3-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="5c3e3-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5c3e3-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
