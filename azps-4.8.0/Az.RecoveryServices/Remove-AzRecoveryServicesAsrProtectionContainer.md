---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182716"
---
# <span data-ttu-id="053d0-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="053d0-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="053d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="053d0-102">SYNOPSIS</span></span>
<span data-ttu-id="053d0-103">Törli a megadott védelmi tárolót a szerkezetéről.</span><span class="sxs-lookup"><span data-stu-id="053d0-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="053d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="053d0-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="053d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="053d0-105">DESCRIPTION</span></span>
<span data-ttu-id="053d0-106">A Remove-AzRecoveryServicesAsrProtectionContainer parancsmag törli a megadott Azure site Recovery Protection tárolót.</span><span class="sxs-lookup"><span data-stu-id="053d0-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="053d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="053d0-107">EXAMPLES</span></span>

### <span data-ttu-id="053d0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="053d0-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="053d0-109">Elindítja a megadott védelmi tároló törlését, és az eltávolítási művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="053d0-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="053d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="053d0-110">PARAMETERS</span></span>

### <span data-ttu-id="053d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="053d0-111">-DefaultProfile</span></span>
<span data-ttu-id="053d0-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="053d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="053d0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="053d0-113">-InputObject</span></span>
<span data-ttu-id="053d0-114">Az eltávolítani kívánt védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="053d0-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="053d0-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="053d0-115">-Confirm</span></span>
<span data-ttu-id="053d0-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="053d0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="053d0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="053d0-117">-WhatIf</span></span>
<span data-ttu-id="053d0-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="053d0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="053d0-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="053d0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="053d0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="053d0-120">CommonParameters</span></span>
<span data-ttu-id="053d0-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="053d0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="053d0-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="053d0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="053d0-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="053d0-123">INPUTS</span></span>

### <span data-ttu-id="053d0-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="053d0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="053d0-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="053d0-125">OUTPUTS</span></span>

### <span data-ttu-id="053d0-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="053d0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="053d0-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="053d0-127">NOTES</span></span>

## <span data-ttu-id="053d0-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="053d0-128">RELATED LINKS</span></span>
