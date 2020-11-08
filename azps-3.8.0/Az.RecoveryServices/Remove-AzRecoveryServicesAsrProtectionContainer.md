---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012640"
---
# <span data-ttu-id="d6479-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d6479-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d6479-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6479-102">SYNOPSIS</span></span>
<span data-ttu-id="d6479-103">Törli a megadott védelmi tárolót a szerkezetéről.</span><span class="sxs-lookup"><span data-stu-id="d6479-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="d6479-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6479-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6479-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6479-105">DESCRIPTION</span></span>
<span data-ttu-id="d6479-106">A Remove-AzRecoveryServicesAsrProtectionContainer parancsmag törli a megadott Azure site Recovery Protection tárolót.</span><span class="sxs-lookup"><span data-stu-id="d6479-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d6479-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6479-107">EXAMPLES</span></span>

### <span data-ttu-id="d6479-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6479-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="d6479-109">Elindítja a megadott védelmi tároló törlését, és az eltávolítási művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d6479-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="d6479-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6479-110">PARAMETERS</span></span>

### <span data-ttu-id="d6479-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6479-111">-DefaultProfile</span></span>
<span data-ttu-id="d6479-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6479-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6479-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6479-113">-InputObject</span></span>
<span data-ttu-id="d6479-114">Az eltávolítani kívánt védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6479-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="d6479-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6479-115">-Confirm</span></span>
<span data-ttu-id="d6479-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6479-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6479-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6479-117">-WhatIf</span></span>
<span data-ttu-id="d6479-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6479-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6479-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6479-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6479-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6479-120">CommonParameters</span></span>
<span data-ttu-id="d6479-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6479-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6479-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6479-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6479-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6479-123">INPUTS</span></span>

### <span data-ttu-id="d6479-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d6479-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d6479-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6479-125">OUTPUTS</span></span>

### <span data-ttu-id="d6479-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d6479-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d6479-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6479-127">NOTES</span></span>

## <span data-ttu-id="d6479-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6479-128">RELATED LINKS</span></span>
