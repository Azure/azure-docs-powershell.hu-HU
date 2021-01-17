---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468677"
---
# <span data-ttu-id="e5a09-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5a09-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="e5a09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a09-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a09-103">AsR-tárbesorolási megfeleltetést hoz létre a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="e5a09-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="e5a09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5a09-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a09-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5a09-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a09-106">A **New-AzRecoveryServicesAsrStorageClassificationMapping** parancsmag létrehoz egy tárolási besorolást a helyreállítási szolgáltatások tárolója megfeleltetésének.</span><span class="sxs-lookup"><span data-stu-id="e5a09-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="e5a09-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5a09-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a09-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e5a09-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="e5a09-109">Megkezdi a tárbesorolási leképezési műveletet a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="e5a09-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e5a09-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5a09-110">PARAMETERS</span></span>

### <span data-ttu-id="e5a09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a09-111">-DefaultProfile</span></span>
<span data-ttu-id="e5a09-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5a09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e5a09-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e5a09-113">-Name</span></span>
<span data-ttu-id="e5a09-114">Megadja az ASR-tárolóbesorolás megfeleltetésének nevét.</span><span class="sxs-lookup"><span data-stu-id="e5a09-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="e5a09-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e5a09-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="e5a09-116">A megfeleltetés elsődleges ASR-tárolóbesorolási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5a09-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a09-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e5a09-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="e5a09-118">A leképezés helyreállítási ASR-tárolóbesorolási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5a09-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a09-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5a09-119">-Confirm</span></span>
<span data-ttu-id="e5a09-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e5a09-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a09-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a09-121">-WhatIf</span></span>
<span data-ttu-id="e5a09-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e5a09-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5a09-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5a09-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a09-124">CommonParameters</span></span>
<span data-ttu-id="e5a09-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a09-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5a09-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a09-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5a09-127">INPUTS</span></span>

### <span data-ttu-id="e5a09-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e5a09-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="e5a09-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5a09-129">OUTPUTS</span></span>

### <span data-ttu-id="e5a09-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="e5a09-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e5a09-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5a09-131">NOTES</span></span>

## <span data-ttu-id="e5a09-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5a09-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5a09-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5a09-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="e5a09-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5a09-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
