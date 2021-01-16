---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355674"
---
# <span data-ttu-id="3a75c-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3a75c-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3a75c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a75c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a75c-103">Törli a megadott ASR-hálózatleképezést a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="3a75c-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="3a75c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a75c-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a75c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a75c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a75c-106">A **Remove-AzRecoveryServicesAsrNetworkMapping** parancsmag törli a megadott ASR-hálózatleképezést.</span><span class="sxs-lookup"><span data-stu-id="3a75c-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="3a75c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a75c-107">EXAMPLES</span></span>

### <span data-ttu-id="3a75c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3a75c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="3a75c-109">Elindítja a megadott ASR-hálózatleképezés törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="3a75c-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3a75c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a75c-110">PARAMETERS</span></span>

### <span data-ttu-id="3a75c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a75c-111">-DefaultProfile</span></span>
<span data-ttu-id="3a75c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a75c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3a75c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a75c-113">-InputObject</span></span>
<span data-ttu-id="3a75c-114">A parancsmag bemeneti objektuma: A törölni szükséges ASR-hálózatleképezésnek megfelelő ASR-hálózati leképezési objektum.</span><span class="sxs-lookup"><span data-stu-id="3a75c-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a75c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a75c-115">-Confirm</span></span>
<span data-ttu-id="3a75c-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3a75c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a75c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a75c-117">-WhatIf</span></span>
<span data-ttu-id="3a75c-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3a75c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a75c-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a75c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a75c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a75c-120">CommonParameters</span></span>
<span data-ttu-id="3a75c-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a75c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a75c-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a75c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a75c-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a75c-123">INPUTS</span></span>

### <span data-ttu-id="3a75c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3a75c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="3a75c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a75c-125">OUTPUTS</span></span>

### <span data-ttu-id="3a75c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="3a75c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3a75c-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a75c-127">NOTES</span></span>

## <span data-ttu-id="3a75c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a75c-128">RELATED LINKS</span></span>

[<span data-ttu-id="3a75c-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3a75c-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3a75c-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3a75c-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
