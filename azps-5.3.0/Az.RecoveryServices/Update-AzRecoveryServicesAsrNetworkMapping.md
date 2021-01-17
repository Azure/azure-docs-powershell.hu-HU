---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467234"
---
# <span data-ttu-id="63ba6-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="63ba6-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="63ba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="63ba6-103">Frissíti a megadott Azure-webhely-helyreállítási hálózat megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="63ba6-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="63ba6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63ba6-104">SYNTAX</span></span>

### <span data-ttu-id="63ba6-105">ByNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63ba6-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63ba6-106">ById</span><span class="sxs-lookup"><span data-stu-id="63ba6-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63ba6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63ba6-107">DESCRIPTION</span></span>
<span data-ttu-id="63ba6-108">Az **Update-AzRecoveryServicesAsrNetworkMapping** parancsmag frissíti a megadott Azure Site Recovery hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="63ba6-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="63ba6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63ba6-109">EXAMPLES</span></span>

### <span data-ttu-id="63ba6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="63ba6-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="63ba6-111">Elindítja a hálózatleképezést a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="63ba6-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="63ba6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63ba6-112">PARAMETERS</span></span>

### <span data-ttu-id="63ba6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ba6-113">-DefaultProfile</span></span>
<span data-ttu-id="63ba6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63ba6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="63ba6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63ba6-115">-InputObject</span></span>
<span data-ttu-id="63ba6-116">Bemeneti objektum: Azt az ASR hálózati leképezési objektumot adja meg, amely megfelel a frissíthető ASR-hálózatleképezésnek.</span><span class="sxs-lookup"><span data-stu-id="63ba6-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="63ba6-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="63ba6-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="63ba6-118">A hálózati megfeleltetés helyreállítási Azure-hálózatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63ba6-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ba6-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="63ba6-119">-RecoveryNetwork</span></span>
<span data-ttu-id="63ba6-120">A hálózati megfeleltetés helyreállítási hálózati objektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="63ba6-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ba6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63ba6-121">-Confirm</span></span>
<span data-ttu-id="63ba6-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="63ba6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ba6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ba6-123">-WhatIf</span></span>
<span data-ttu-id="63ba6-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="63ba6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63ba6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63ba6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ba6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ba6-126">CommonParameters</span></span>
<span data-ttu-id="63ba6-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63ba6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ba6-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63ba6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ba6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63ba6-129">INPUTS</span></span>

### <span data-ttu-id="63ba6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="63ba6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="63ba6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63ba6-131">OUTPUTS</span></span>

### <span data-ttu-id="63ba6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="63ba6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="63ba6-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63ba6-133">NOTES</span></span>

## <span data-ttu-id="63ba6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63ba6-134">RELATED LINKS</span></span>
