---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d19455e4b467846ce38541ca3b0ec02f586cf226
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927633"
---
# <span data-ttu-id="2d03f-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="2d03f-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="2d03f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d03f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d03f-103">Egy regisztrált vCenter felderítési részleteinek frissítése.</span><span class="sxs-lookup"><span data-stu-id="2d03f-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="2d03f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d03f-104">SYNTAX</span></span>

### <span data-ttu-id="2d03f-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d03f-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d03f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2d03f-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d03f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d03f-107">DESCRIPTION</span></span>
<span data-ttu-id="2d03f-108">Az **Update-AzRecoveryServicesAsrvCenter** parancsmag egy regisztrált vCenter felderítési részleteinek frissítése.</span><span class="sxs-lookup"><span data-stu-id="2d03f-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="2d03f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d03f-109">EXAMPLES</span></span>

### <span data-ttu-id="2d03f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2d03f-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="2d03f-111">Egy regisztrált vCenter felderítési részleteinek frissítése.</span><span class="sxs-lookup"><span data-stu-id="2d03f-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="2d03f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d03f-112">PARAMETERS</span></span>

### <span data-ttu-id="2d03f-113">-Account</span><span class="sxs-lookup"><span data-stu-id="2d03f-113">-Account</span></span>
<span data-ttu-id="2d03f-114">vCenter bejelentkezési hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="2d03f-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="2d03f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d03f-115">-DefaultProfile</span></span>
<span data-ttu-id="2d03f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d03f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d03f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d03f-117">-InputObject</span></span>
<span data-ttu-id="2d03f-118">A vCenter-kiszolgálóobjektum, amelyről frissítheti a feltárási adatokat.</span><span class="sxs-lookup"><span data-stu-id="2d03f-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="2d03f-119">-Port</span><span class="sxs-lookup"><span data-stu-id="2d03f-119">-Port</span></span>
<span data-ttu-id="2d03f-120">A feltáráshoz használt TCP-port a vCenter-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2d03f-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="2d03f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d03f-121">-ResourceId</span></span>
<span data-ttu-id="2d03f-122">A vCenter erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d03f-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="2d03f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d03f-123">-Confirm</span></span>
<span data-ttu-id="2d03f-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2d03f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d03f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d03f-125">-WhatIf</span></span>
<span data-ttu-id="2d03f-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2d03f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d03f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d03f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d03f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d03f-128">CommonParameters</span></span>
<span data-ttu-id="2d03f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d03f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d03f-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d03f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d03f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d03f-131">INPUTS</span></span>

### <span data-ttu-id="2d03f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2d03f-132">System.String</span></span>

### <span data-ttu-id="2d03f-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="2d03f-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="2d03f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d03f-134">OUTPUTS</span></span>

### <span data-ttu-id="2d03f-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="2d03f-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2d03f-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d03f-136">NOTES</span></span>

## <span data-ttu-id="2d03f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d03f-137">RELATED LINKS</span></span>
