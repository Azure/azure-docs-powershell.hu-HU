---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206183"
---
# <span data-ttu-id="f7140-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f7140-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f7140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7140-102">SYNOPSIS</span></span>
<span data-ttu-id="f7140-103">Törli a megadott ASR-tárterületbesorolás megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="f7140-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="f7140-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7140-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7140-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7140-105">DESCRIPTION</span></span>
<span data-ttu-id="f7140-106">A **Remove-AzRecoveryServicesAsrStorageClassificationMapping** parancsmag törli a megadott Azure-webhely-helyreállítás tárbesorolási megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="f7140-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="f7140-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7140-107">EXAMPLES</span></span>

### <span data-ttu-id="f7140-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7140-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="f7140-109">Elindítja a megadott tárbesorolási megfeleltetés törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="f7140-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f7140-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7140-110">PARAMETERS</span></span>

### <span data-ttu-id="f7140-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7140-111">-DefaultProfile</span></span>
<span data-ttu-id="f7140-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7140-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f7140-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7140-113">-InputObject</span></span>
<span data-ttu-id="f7140-114">A parancsmag bemeneti objektuma: Az ASR tárbesorolási megfeleltetési objektuma, amely megfelel a törölni szükséges ASR-tárbesorolás megfeleltetésének.</span><span class="sxs-lookup"><span data-stu-id="f7140-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="f7140-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7140-115">-Confirm</span></span>
<span data-ttu-id="f7140-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f7140-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7140-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7140-117">-WhatIf</span></span>
<span data-ttu-id="f7140-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f7140-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7140-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7140-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7140-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7140-120">CommonParameters</span></span>
<span data-ttu-id="f7140-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7140-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7140-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7140-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7140-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7140-123">INPUTS</span></span>

### <span data-ttu-id="f7140-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f7140-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="f7140-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7140-125">OUTPUTS</span></span>

### <span data-ttu-id="f7140-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="f7140-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f7140-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7140-127">NOTES</span></span>

## <span data-ttu-id="f7140-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7140-128">RELATED LINKS</span></span>

[<span data-ttu-id="f7140-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f7140-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f7140-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f7140-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
