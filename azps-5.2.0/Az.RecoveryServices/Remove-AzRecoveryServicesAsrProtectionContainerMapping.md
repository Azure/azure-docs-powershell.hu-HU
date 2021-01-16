---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355650"
---
# <span data-ttu-id="418de-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="418de-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="418de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="418de-102">SYNOPSIS</span></span>
<span data-ttu-id="418de-103">Törli a megadott Azure Site Recovery Protection tárolóleképezést.</span><span class="sxs-lookup"><span data-stu-id="418de-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="418de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="418de-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="418de-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="418de-105">DESCRIPTION</span></span>
<span data-ttu-id="418de-106">A **Remove-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag törli a megadott Azure Site Recovery Protection tárolóleképezést.</span><span class="sxs-lookup"><span data-stu-id="418de-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="418de-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="418de-107">EXAMPLES</span></span>

### <span data-ttu-id="418de-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="418de-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="418de-109">Elindítja a megadott védelmi tároló megfeleltetésének törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="418de-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="418de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="418de-110">PARAMETERS</span></span>

### <span data-ttu-id="418de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418de-111">-DefaultProfile</span></span>
<span data-ttu-id="418de-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="418de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="418de-113">-Force</span><span class="sxs-lookup"><span data-stu-id="418de-113">-Force</span></span>
<span data-ttu-id="418de-114">A parancs futtatását további figyelmeztetés nélkül kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="418de-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418de-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="418de-115">-InputObject</span></span>
<span data-ttu-id="418de-116">A parancsmag bemeneti objektuma: a törölni szükséges védelmi tárolónak megfelelő ASR védelmi tárolóleképezés objektum.</span><span class="sxs-lookup"><span data-stu-id="418de-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="418de-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="418de-117">-Confirm</span></span>
<span data-ttu-id="418de-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="418de-118">Specify if confirmation is required.</span></span> <span data-ttu-id="418de-119">A megerősítési paraméter értékének $false a megerősítés kihagyása érdekében</span><span class="sxs-lookup"><span data-stu-id="418de-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="418de-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418de-120">-WhatIf</span></span>
<span data-ttu-id="418de-121">Azt mutatja meg, mi történik, ha a parancsmag végrehajtása a parancsmag végrehajtása nélkül történik.</span><span class="sxs-lookup"><span data-stu-id="418de-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="418de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418de-122">CommonParameters</span></span>
<span data-ttu-id="418de-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="418de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418de-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="418de-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418de-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="418de-125">INPUTS</span></span>

### <span data-ttu-id="418de-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="418de-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="418de-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="418de-127">OUTPUTS</span></span>

### <span data-ttu-id="418de-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="418de-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="418de-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="418de-129">NOTES</span></span>

## <span data-ttu-id="418de-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="418de-130">RELATED LINKS</span></span>

[<span data-ttu-id="418de-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="418de-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="418de-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="418de-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
