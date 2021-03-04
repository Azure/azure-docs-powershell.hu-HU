---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f7d71d0e69f83633d02832bd3f54554be1fa0ba0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919241"
---
# <span data-ttu-id="9f62b-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9f62b-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="9f62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f62b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f62b-103">Törli a megadott Azure Site Recovery Protection tárolóleképezést.</span><span class="sxs-lookup"><span data-stu-id="9f62b-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="9f62b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f62b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f62b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f62b-105">DESCRIPTION</span></span>
<span data-ttu-id="9f62b-106">A **Remove-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag törli a megadott Azure-webhely-helyreállítás elleni védelem tárolóleképezését.</span><span class="sxs-lookup"><span data-stu-id="9f62b-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="9f62b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f62b-107">EXAMPLES</span></span>

### <span data-ttu-id="9f62b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9f62b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="9f62b-109">Elindítja a megadott védelmi tárolóleképezés törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9f62b-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9f62b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f62b-110">PARAMETERS</span></span>

### <span data-ttu-id="9f62b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f62b-111">-DefaultProfile</span></span>
<span data-ttu-id="9f62b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f62b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9f62b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9f62b-113">-Force</span></span>
<span data-ttu-id="9f62b-114">A parancs futtatását további figyelmeztetés nélkül kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="9f62b-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="9f62b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f62b-115">-InputObject</span></span>
<span data-ttu-id="9f62b-116">A parancsmag bemeneti objektuma: a törölni szükséges védelmi tárolónak megfelelő ASR védelmi tárolóleképezés objektum.</span><span class="sxs-lookup"><span data-stu-id="9f62b-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="9f62b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f62b-117">-Confirm</span></span>
<span data-ttu-id="9f62b-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="9f62b-118">Specify if confirmation is required.</span></span> <span data-ttu-id="9f62b-119">A megerősítési paraméter értékének $false a megerősítés kihagyása érdekében</span><span class="sxs-lookup"><span data-stu-id="9f62b-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="9f62b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f62b-120">-WhatIf</span></span>
<span data-ttu-id="9f62b-121">Azt mutatja meg, mi történik, ha a parancsmag végrehajtása a parancsmag végrehajtása nélkül történik.</span><span class="sxs-lookup"><span data-stu-id="9f62b-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="9f62b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f62b-122">CommonParameters</span></span>
<span data-ttu-id="9f62b-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f62b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f62b-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f62b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f62b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f62b-125">INPUTS</span></span>

### <span data-ttu-id="9f62b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9f62b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="9f62b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f62b-127">OUTPUTS</span></span>

### <span data-ttu-id="9f62b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="9f62b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9f62b-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f62b-129">NOTES</span></span>

## <span data-ttu-id="9f62b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f62b-130">RELATED LINKS</span></span>

[<span data-ttu-id="9f62b-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9f62b-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="9f62b-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9f62b-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
