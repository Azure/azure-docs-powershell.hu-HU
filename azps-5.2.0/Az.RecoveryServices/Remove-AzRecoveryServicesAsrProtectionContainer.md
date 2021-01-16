---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355661"
---
# <span data-ttu-id="7a4a7-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7a4a7-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="7a4a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7a4a7-103">Törli a megadott védelmi tárolót a szövetből.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="7a4a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a4a7-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a4a7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a4a7-105">DESCRIPTION</span></span>
<span data-ttu-id="7a4a7-106">A Remove-AzRecoveryServicesAsrProtectionContainer parancsmag törli a megadott Azure Webhely-helyreállításvédelmi tárolót.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="7a4a7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a4a7-107">EXAMPLES</span></span>

### <span data-ttu-id="7a4a7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a4a7-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="7a4a7-109">Elindítja a megadott védelmi tároló törlését, és visszaadja az eltávolítási művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="7a4a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a4a7-110">PARAMETERS</span></span>

### <span data-ttu-id="7a4a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a4a7-111">-DefaultProfile</span></span>
<span data-ttu-id="7a4a7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a4a7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a4a7-113">-InputObject</span></span>
<span data-ttu-id="7a4a7-114">Az eltávolítható védelmi tároló.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4a7-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a4a7-115">-Confirm</span></span>
<span data-ttu-id="7a4a7-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a4a7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a4a7-117">-WhatIf</span></span>
<span data-ttu-id="7a4a7-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a4a7-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a4a7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a4a7-120">CommonParameters</span></span>
<span data-ttu-id="7a4a7-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a4a7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a4a7-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a4a7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a4a7-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a4a7-123">INPUTS</span></span>

### <span data-ttu-id="7a4a7-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7a4a7-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="7a4a7-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a4a7-125">OUTPUTS</span></span>

### <span data-ttu-id="7a4a7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="7a4a7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7a4a7-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a4a7-127">NOTES</span></span>

## <span data-ttu-id="7a4a7-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a4a7-128">RELATED LINKS</span></span>
