---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: b19808ff7b5576c93bc81414d665e23086e524d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919185"
---
# <span data-ttu-id="ab41d-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ab41d-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ab41d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab41d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab41d-103">Törli a megadott ASR-tárterületbesorolás megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="ab41d-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="ab41d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab41d-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab41d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab41d-105">DESCRIPTION</span></span>
<span data-ttu-id="ab41d-106">A **Remove-AzRecoveryServicesAsrStorageClassificationMapping** parancsmag törli a megadott Azure-webhely-helyreállítás tárbesorolási megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="ab41d-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="ab41d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab41d-107">EXAMPLES</span></span>

### <span data-ttu-id="ab41d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ab41d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="ab41d-109">Elindítja a megadott tárbesorolási megfeleltetés törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="ab41d-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ab41d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab41d-110">PARAMETERS</span></span>

### <span data-ttu-id="ab41d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab41d-111">-DefaultProfile</span></span>
<span data-ttu-id="ab41d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab41d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ab41d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab41d-113">-InputObject</span></span>
<span data-ttu-id="ab41d-114">A parancsmag bemeneti objektuma: Az ASR tárbesorolás megfeleltetési objektuma, amely megfelel a törölni szükséges ASR-tárbesorolás megfeleltetésének.</span><span class="sxs-lookup"><span data-stu-id="ab41d-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab41d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab41d-115">-Confirm</span></span>
<span data-ttu-id="ab41d-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ab41d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab41d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab41d-117">-WhatIf</span></span>
<span data-ttu-id="ab41d-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ab41d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab41d-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab41d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab41d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab41d-120">CommonParameters</span></span>
<span data-ttu-id="ab41d-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab41d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab41d-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab41d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab41d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab41d-123">INPUTS</span></span>

### <span data-ttu-id="ab41d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ab41d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="ab41d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab41d-125">OUTPUTS</span></span>

### <span data-ttu-id="ab41d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="ab41d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ab41d-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab41d-127">NOTES</span></span>

## <span data-ttu-id="ab41d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab41d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ab41d-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ab41d-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ab41d-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ab41d-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
