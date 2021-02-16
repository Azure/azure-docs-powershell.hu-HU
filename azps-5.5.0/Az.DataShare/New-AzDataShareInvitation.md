---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166019"
---
# <span data-ttu-id="97fce-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="97fce-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="97fce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97fce-102">SYNOPSIS</span></span>
<span data-ttu-id="97fce-103">Megosztásra szóló meghívót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="97fce-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="97fce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97fce-104">SYNTAX</span></span>

### <span data-ttu-id="97fce-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97fce-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97fce-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="97fce-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97fce-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="97fce-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97fce-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97fce-108">DESCRIPTION</span></span>
<span data-ttu-id="97fce-109">A **New-AzDataShareInvitation** parancsmag meghívót küld a cél felhasználónak a szolgáltató megosztásáról.</span><span class="sxs-lookup"><span data-stu-id="97fce-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="97fce-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97fce-110">EXAMPLES</span></span>

### <span data-ttu-id="97fce-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="97fce-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="97fce-112">Ez a parancs meghívót hoz létre az AdsShare megosztásához, és elküldi azt a célzott e-mail-címre. adstest@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="97fce-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="97fce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97fce-113">PARAMETERS</span></span>

### <span data-ttu-id="97fce-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97fce-114">-AccountName</span></span>
<span data-ttu-id="97fce-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="97fce-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97fce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fce-116">-DefaultProfile</span></span>
<span data-ttu-id="97fce-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97fce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97fce-118">-Name</span><span class="sxs-lookup"><span data-stu-id="97fce-118">-Name</span></span>
<span data-ttu-id="97fce-119">Azure-adatok megosztására szóló meghívó neve</span><span class="sxs-lookup"><span data-stu-id="97fce-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97fce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97fce-120">-ResourceGroupName</span></span>
<span data-ttu-id="97fce-121">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="97fce-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97fce-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="97fce-122">-ShareName</span></span>
<span data-ttu-id="97fce-123">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="97fce-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97fce-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="97fce-124">-TargetEmail</span></span>
<span data-ttu-id="97fce-125">Cél e-mail-azonosító</span><span class="sxs-lookup"><span data-stu-id="97fce-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97fce-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="97fce-126">-TargetObjectId</span></span>
<span data-ttu-id="97fce-127">Célobjektum-azonosító</span><span class="sxs-lookup"><span data-stu-id="97fce-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97fce-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="97fce-128">-TargetTenantId</span></span>
<span data-ttu-id="97fce-129">Cél bérlőazonosító</span><span class="sxs-lookup"><span data-stu-id="97fce-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97fce-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97fce-130">-Confirm</span></span>
<span data-ttu-id="97fce-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="97fce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97fce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97fce-132">-WhatIf</span></span>
<span data-ttu-id="97fce-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="97fce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97fce-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97fce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97fce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fce-135">CommonParameters</span></span>
<span data-ttu-id="97fce-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97fce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fce-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97fce-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fce-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97fce-138">INPUTS</span></span>

### <span data-ttu-id="97fce-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="97fce-139">None</span></span>

## <span data-ttu-id="97fce-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97fce-140">OUTPUTS</span></span>

### <span data-ttu-id="97fce-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="97fce-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="97fce-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97fce-142">NOTES</span></span>

## <span data-ttu-id="97fce-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97fce-143">RELATED LINKS</span></span>
