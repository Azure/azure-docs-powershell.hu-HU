---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186857"
---
# <span data-ttu-id="9cb3b-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9cb3b-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="9cb3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb3b-103">Azure-webhely-helyreállítási szövetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="9cb3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cb3b-104">SYNTAX</span></span>

### <span data-ttu-id="9cb3b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cb3b-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb3b-106">Azure</span><span class="sxs-lookup"><span data-stu-id="9cb3b-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb3b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cb3b-107">DESCRIPTION</span></span>
<span data-ttu-id="9cb3b-108">A **New-AzRecoveryServicesAsrFabric** parancsmag a megadott típusú Azure webhely-helyreállítási szerkezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="9cb3b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9cb3b-109">EXAMPLES</span></span>

### <span data-ttu-id="9cb3b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9cb3b-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="9cb3b-111">Az átadott névvel elindítja a szerkezet-készítést, és visszaadja a kelme-létrehozási művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="9cb3b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9cb3b-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="9cb3b-113">Elindítja az Azure Fabric-készítést az átadott névvel, és visszaadja a szerkezet létrehozásának műveletének nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="9cb3b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cb3b-114">PARAMETERS</span></span>

### <span data-ttu-id="9cb3b-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="9cb3b-115">-Azure</span></span>
<span data-ttu-id="9cb3b-116">A kapcsoló paraméterrel az Azure-szövet hozható létre.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="9cb3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb3b-117">-DefaultProfile</span></span>
<span data-ttu-id="9cb3b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9cb3b-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="9cb3b-119">-Location</span></span>
<span data-ttu-id="9cb3b-120">A létrehozott anyag objektumnak megfelelő Azure-régiót adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="9cb3b-121">Az Azure site Recovery Fabric objektum a régiót jelöli.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="9cb3b-122">Két Azure-régió közötti replikálást szolgáló virtuális gépek esetében az elsődleges anyag az elsődleges Azure-régió és a helyreállítási anyag.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="9cb3b-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cb3b-123">-Name</span></span>
<span data-ttu-id="9cb3b-124">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="9cb3b-125">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="9cb3b-125">-Type</span></span>
<span data-ttu-id="9cb3b-126">Az Azure webhely-helyreállítási anyag típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="9cb3b-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cb3b-127">-Confirm</span></span>
<span data-ttu-id="9cb3b-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb3b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb3b-129">-WhatIf</span></span>
<span data-ttu-id="9cb3b-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cb3b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb3b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb3b-132">CommonParameters</span></span>
<span data-ttu-id="9cb3b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cb3b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb3b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9cb3b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb3b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cb3b-135">INPUTS</span></span>

### <span data-ttu-id="9cb3b-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="9cb3b-136">None</span></span>

## <span data-ttu-id="9cb3b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cb3b-137">OUTPUTS</span></span>

### <span data-ttu-id="9cb3b-138">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9cb3b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9cb3b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cb3b-139">NOTES</span></span>

## <span data-ttu-id="9cb3b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cb3b-140">RELATED LINKS</span></span>

[<span data-ttu-id="9cb3b-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9cb3b-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="9cb3b-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9cb3b-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
