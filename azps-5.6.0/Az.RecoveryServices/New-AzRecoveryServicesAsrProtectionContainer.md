---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 22ade5e749909683ff2de93065ccf458ab2ec73f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920970"
---
# <span data-ttu-id="f02f1-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f02f1-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="f02f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f02f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f02f1-103">Létrehoz egy Azure Site Recovery Protection tárolót a megadott anyagon belül.</span><span class="sxs-lookup"><span data-stu-id="f02f1-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="f02f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f02f1-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f02f1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f02f1-105">DESCRIPTION</span></span>
<span data-ttu-id="f02f1-106">A New-AzRecoveryServicesAsrProtectionContainer parancsmag létrehoz egy védelmi tárolót a megadott Azure Site Recovery Fabric alatt.</span><span class="sxs-lookup"><span data-stu-id="f02f1-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="f02f1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f02f1-107">EXAMPLES</span></span>

### <span data-ttu-id="f02f1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f02f1-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="f02f1-109">Elindítja a védelmi tároló létrehozását a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="f02f1-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f02f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f02f1-110">PARAMETERS</span></span>

### <span data-ttu-id="f02f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02f1-111">-DefaultProfile</span></span>
<span data-ttu-id="f02f1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f02f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f02f1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f02f1-113">-InputObject</span></span>
<span data-ttu-id="f02f1-114">Létrehozza a replikációvédelmi tárolót a megadott bemeneti objektumban (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="f02f1-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f02f1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f02f1-115">-Name</span></span>
<span data-ttu-id="f02f1-116">A védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="f02f1-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="f02f1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f02f1-117">-Confirm</span></span>
<span data-ttu-id="f02f1-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f02f1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f02f1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f02f1-119">-WhatIf</span></span>
<span data-ttu-id="f02f1-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f02f1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f02f1-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f02f1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f02f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02f1-122">CommonParameters</span></span>
<span data-ttu-id="f02f1-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02f1-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f02f1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02f1-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f02f1-125">INPUTS</span></span>

### <span data-ttu-id="f02f1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f02f1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f02f1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f02f1-127">OUTPUTS</span></span>

### <span data-ttu-id="f02f1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="f02f1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f02f1-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f02f1-129">NOTES</span></span>

## <span data-ttu-id="f02f1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f02f1-130">RELATED LINKS</span></span>
