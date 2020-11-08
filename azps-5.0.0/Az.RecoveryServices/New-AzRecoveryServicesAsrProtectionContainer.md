---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: fecc6f1911a82b20d3f96643ceed83486727f29f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186565"
---
# <span data-ttu-id="4016c-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4016c-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="4016c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4016c-102">SYNOPSIS</span></span>
<span data-ttu-id="4016c-103">Azure site Recovery Protection tárolót hoz létre a megadott szerkezeten belül.</span><span class="sxs-lookup"><span data-stu-id="4016c-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="4016c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4016c-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4016c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4016c-105">DESCRIPTION</span></span>
<span data-ttu-id="4016c-106">Az New-AzRecoveryServicesAsrProtectionContainer parancsmag egy védelmi tárolót hoz létre a megadott Azure webhely-helyreállítási anyagban.</span><span class="sxs-lookup"><span data-stu-id="4016c-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="4016c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4016c-107">EXAMPLES</span></span>

### <span data-ttu-id="4016c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4016c-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="4016c-109">Elindítja a védett tároló létrehozását a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4016c-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4016c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4016c-110">PARAMETERS</span></span>

### <span data-ttu-id="4016c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4016c-111">-DefaultProfile</span></span>
<span data-ttu-id="4016c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4016c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4016c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4016c-113">-InputObject</span></span>
<span data-ttu-id="4016c-114">A Replication Protection tárolót hozza létre a megadott bemeneti objektumban (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="4016c-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="4016c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4016c-115">-Name</span></span>
<span data-ttu-id="4016c-116">A védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="4016c-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="4016c-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4016c-117">-Confirm</span></span>
<span data-ttu-id="4016c-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4016c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4016c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4016c-119">-WhatIf</span></span>
<span data-ttu-id="4016c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4016c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4016c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4016c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4016c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4016c-122">CommonParameters</span></span>
<span data-ttu-id="4016c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4016c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4016c-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4016c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4016c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4016c-125">INPUTS</span></span>

### <span data-ttu-id="4016c-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4016c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4016c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4016c-127">OUTPUTS</span></span>

### <span data-ttu-id="4016c-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4016c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4016c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4016c-129">NOTES</span></span>

## <span data-ttu-id="4016c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4016c-130">RELATED LINKS</span></span>
