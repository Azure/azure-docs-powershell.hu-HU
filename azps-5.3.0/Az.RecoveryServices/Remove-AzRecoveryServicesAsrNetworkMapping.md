---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468642"
---
# <span data-ttu-id="735d9-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="735d9-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="735d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="735d9-102">SYNOPSIS</span></span>
<span data-ttu-id="735d9-103">Törli a megadott ASR-hálózatleképezést a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="735d9-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="735d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="735d9-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="735d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="735d9-105">DESCRIPTION</span></span>
<span data-ttu-id="735d9-106">A **Remove-AzRecoveryServicesAsrNetworkMapping** parancsmag törli a megadott ASR-hálózatleképezést.</span><span class="sxs-lookup"><span data-stu-id="735d9-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="735d9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="735d9-107">EXAMPLES</span></span>

### <span data-ttu-id="735d9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="735d9-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="735d9-109">Elindítja a megadott ASR-hálózatleképezés törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="735d9-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="735d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="735d9-110">PARAMETERS</span></span>

### <span data-ttu-id="735d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735d9-111">-DefaultProfile</span></span>
<span data-ttu-id="735d9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="735d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="735d9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="735d9-113">-InputObject</span></span>
<span data-ttu-id="735d9-114">A parancsmag bemeneti objektuma: A törölni szükséges ASR-hálózatleképezésnek megfelelő ASR-hálózati leképezési objektum.</span><span class="sxs-lookup"><span data-stu-id="735d9-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="735d9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="735d9-115">-Confirm</span></span>
<span data-ttu-id="735d9-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="735d9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="735d9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="735d9-117">-WhatIf</span></span>
<span data-ttu-id="735d9-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="735d9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="735d9-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="735d9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="735d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735d9-120">CommonParameters</span></span>
<span data-ttu-id="735d9-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735d9-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="735d9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735d9-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="735d9-123">INPUTS</span></span>

### <span data-ttu-id="735d9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="735d9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="735d9-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="735d9-125">OUTPUTS</span></span>

### <span data-ttu-id="735d9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="735d9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="735d9-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="735d9-127">NOTES</span></span>

## <span data-ttu-id="735d9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="735d9-128">RELATED LINKS</span></span>

[<span data-ttu-id="735d9-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="735d9-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="735d9-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="735d9-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
