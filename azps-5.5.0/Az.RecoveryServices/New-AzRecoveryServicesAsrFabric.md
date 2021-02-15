---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160122"
---
# <span data-ttu-id="4ac97-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4ac97-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="4ac97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac97-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac97-103">Létrehoz egy Azure-webhely helyreállítási anyagát.</span><span class="sxs-lookup"><span data-stu-id="4ac97-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="4ac97-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ac97-104">SYNTAX</span></span>

### <span data-ttu-id="4ac97-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ac97-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ac97-106">Azure</span><span class="sxs-lookup"><span data-stu-id="4ac97-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac97-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ac97-107">DESCRIPTION</span></span>
<span data-ttu-id="4ac97-108">A **New-AzRecoveryServicesAsrFabric** parancsmag létrehoz egy megadott típusú Azure Site Recovery Fabricot.</span><span class="sxs-lookup"><span data-stu-id="4ac97-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="4ac97-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ac97-109">EXAMPLES</span></span>

### <span data-ttu-id="4ac97-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4ac97-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="4ac97-111">A szövetkészítést a megfelelő névvel kezdi, és visszaadja a szövetkészítés nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="4ac97-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="4ac97-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4ac97-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="4ac97-113">Az Azure Fabric létrehozását a megfelelő névvel kezdi, és visszaadja a szövetkészítési művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="4ac97-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="4ac97-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ac97-114">PARAMETERS</span></span>

### <span data-ttu-id="4ac97-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="4ac97-115">-Azure</span></span>
<span data-ttu-id="4ac97-116">A Kapcsoló paraméter az Azure-anyag létrehozásához ad meg egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="4ac97-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="4ac97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac97-117">-DefaultProfile</span></span>
<span data-ttu-id="4ac97-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ac97-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4ac97-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4ac97-119">-Location</span></span>
<span data-ttu-id="4ac97-120">A létrehozott Fabric objektumnak megfelelő Azure-régiót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ac97-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="4ac97-121">Az Azure Site Recovery szövetobjektum egy régiót képvisel.</span><span class="sxs-lookup"><span data-stu-id="4ac97-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="4ac97-122">Két Azure-régió között replikált virtuális gépek esetében az elsődleges anyag az elsődleges Azure-régiót és a helyreállítási szerkezetet képviseli.</span><span class="sxs-lookup"><span data-stu-id="4ac97-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="4ac97-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4ac97-123">-Name</span></span>
<span data-ttu-id="4ac97-124">Az Azure Site Recovery Fabric nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ac97-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="4ac97-125">-Type</span><span class="sxs-lookup"><span data-stu-id="4ac97-125">-Type</span></span>
<span data-ttu-id="4ac97-126">Az Azure Site Recovery Fabric típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4ac97-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="4ac97-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ac97-127">-Confirm</span></span>
<span data-ttu-id="4ac97-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ac97-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac97-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac97-129">-WhatIf</span></span>
<span data-ttu-id="4ac97-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4ac97-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ac97-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ac97-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac97-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac97-132">CommonParameters</span></span>
<span data-ttu-id="4ac97-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac97-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac97-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ac97-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac97-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ac97-135">INPUTS</span></span>

### <span data-ttu-id="4ac97-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="4ac97-136">None</span></span>

## <span data-ttu-id="4ac97-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ac97-137">OUTPUTS</span></span>

### <span data-ttu-id="4ac97-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="4ac97-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4ac97-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ac97-139">NOTES</span></span>

## <span data-ttu-id="4ac97-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ac97-140">RELATED LINKS</span></span>

[<span data-ttu-id="4ac97-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4ac97-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="4ac97-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4ac97-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
