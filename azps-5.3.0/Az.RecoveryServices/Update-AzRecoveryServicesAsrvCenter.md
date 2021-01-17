---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466640"
---
# <span data-ttu-id="9af20-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="9af20-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="9af20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af20-102">SYNOPSIS</span></span>
<span data-ttu-id="9af20-103">Egy regisztrált vCenter felderítési részleteinek frissítése.</span><span class="sxs-lookup"><span data-stu-id="9af20-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9af20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9af20-104">SYNTAX</span></span>

### <span data-ttu-id="9af20-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9af20-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9af20-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9af20-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9af20-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9af20-107">DESCRIPTION</span></span>
<span data-ttu-id="9af20-108">Az **Update-AzRecoveryServicesAsrvCenter** parancsmag egy regisztrált vCenter felderítési részleteinek frissítése.</span><span class="sxs-lookup"><span data-stu-id="9af20-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9af20-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9af20-109">EXAMPLES</span></span>

### <span data-ttu-id="9af20-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9af20-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="9af20-111">Egy regisztrált vCenter felderítési részleteinek frissítése.</span><span class="sxs-lookup"><span data-stu-id="9af20-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9af20-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9af20-112">PARAMETERS</span></span>

### <span data-ttu-id="9af20-113">-Account</span><span class="sxs-lookup"><span data-stu-id="9af20-113">-Account</span></span>
<span data-ttu-id="9af20-114">vCenter bejelentkezési hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="9af20-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af20-115">-DefaultProfile</span></span>
<span data-ttu-id="9af20-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9af20-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9af20-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9af20-117">-InputObject</span></span>
<span data-ttu-id="9af20-118">A vCenter-kiszolgálóobjektum, amelyről frissítheti a feltárási adatokat.</span><span class="sxs-lookup"><span data-stu-id="9af20-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9af20-119">-Port</span><span class="sxs-lookup"><span data-stu-id="9af20-119">-Port</span></span>
<span data-ttu-id="9af20-120">A feltáráshoz használt TCP-port a vCenter-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="9af20-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af20-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9af20-121">-ResourceId</span></span>
<span data-ttu-id="9af20-122">A vCenter erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9af20-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af20-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9af20-123">-Confirm</span></span>
<span data-ttu-id="9af20-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9af20-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9af20-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af20-125">-WhatIf</span></span>
<span data-ttu-id="9af20-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9af20-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af20-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9af20-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9af20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af20-128">CommonParameters</span></span>
<span data-ttu-id="9af20-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af20-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9af20-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af20-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9af20-131">INPUTS</span></span>

### <span data-ttu-id="9af20-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9af20-132">System.String</span></span>

### <span data-ttu-id="9af20-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="9af20-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="9af20-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9af20-134">OUTPUTS</span></span>

### <span data-ttu-id="9af20-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="9af20-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9af20-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9af20-136">NOTES</span></span>

## <span data-ttu-id="9af20-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9af20-137">RELATED LINKS</span></span>
