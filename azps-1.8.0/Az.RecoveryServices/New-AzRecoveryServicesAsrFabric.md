---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8604d1a648590e0fc88a268e6bf2941bbf9344e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669672"
---
# <span data-ttu-id="d5a6a-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d5a6a-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="d5a6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a6a-103">Azure-webhely-helyreállítási szövetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="d5a6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5a6a-104">SYNTAX</span></span>

### <span data-ttu-id="d5a6a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5a6a-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a6a-106">Azure</span><span class="sxs-lookup"><span data-stu-id="d5a6a-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a6a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5a6a-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a6a-108">A **New-AzRecoveryServicesAsrFabric** parancsmag a megadott típusú Azure webhely-helyreállítási szerkezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="d5a6a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5a6a-109">EXAMPLES</span></span>

### <span data-ttu-id="d5a6a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5a6a-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="d5a6a-111">Az átadott névvel elindítja a szerkezet-készítést, és visszaadja a kelme-létrehozási művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="d5a6a-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d5a6a-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Az -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="d5a6a-113">Elindítja az Azure Fabric-készítést az átadott névvel, és visszaadja a szerkezet létrehozásának műveletének nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="d5a6a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5a6a-114">PARAMETERS</span></span>

### <span data-ttu-id="d5a6a-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="d5a6a-115">-Azure</span></span>
<span data-ttu-id="d5a6a-116">{{Fill Azure Description}}</span><span class="sxs-lookup"><span data-stu-id="d5a6a-116">{{Fill Azure Description}}</span></span>

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

### <span data-ttu-id="d5a6a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a6a-117">-DefaultProfile</span></span>
<span data-ttu-id="d5a6a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d5a6a-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="d5a6a-119">-Location</span></span>
<span data-ttu-id="d5a6a-120">A létrehozott anyag objektumnak megfelelő Azure-régiót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="d5a6a-121">Az Azure site Recovery Fabric objektum a régiót jelöli.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="d5a6a-122">Két Azure-régió közötti replikálást szolgáló virtuális gépek esetében az elsődleges anyag az elsődleges Azure-régió és a helyreállítási anyag.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="d5a6a-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5a6a-123">-Name</span></span>
<span data-ttu-id="d5a6a-124">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="d5a6a-125">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="d5a6a-125">-Type</span></span>
<span data-ttu-id="d5a6a-126">Az Azure webhely-helyreállítási anyag típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="d5a6a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5a6a-127">-Confirm</span></span>
<span data-ttu-id="d5a6a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a6a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a6a-129">-WhatIf</span></span>
<span data-ttu-id="d5a6a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5a6a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5a6a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a6a-132">CommonParameters</span></span>
<span data-ttu-id="d5a6a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5a6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a6a-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a6a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a6a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a6a-135">INPUTS</span></span>

### <span data-ttu-id="d5a6a-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="d5a6a-136">None</span></span>

## <span data-ttu-id="d5a6a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a6a-137">OUTPUTS</span></span>

### <span data-ttu-id="d5a6a-138">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d5a6a-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d5a6a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5a6a-139">NOTES</span></span>

## <span data-ttu-id="d5a6a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5a6a-140">RELATED LINKS</span></span>

[<span data-ttu-id="d5a6a-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d5a6a-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="d5a6a-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d5a6a-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
